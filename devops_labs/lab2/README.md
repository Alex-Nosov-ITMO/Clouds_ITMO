# Лаброраторная работа №2

## Работа с контейнерами Docker. Испольщование good and bad practices в Dockerfile

**Задание:** ***Написать два Dockerfile – плохой и хороший. Плохой должен запускаться и работать корректно, но в нём должно быть не менее 3 “bad practices”. В хорошем Dockerfile они должны быть исправлены. В Readme описать все плохие практики из кода Dockerfile и почему они плохие, как они были исправлены в хорошем  Dockerfile, а также две плохие практики по использованию этого контейнера***


### Создание плохого Dockerfile

![Плохой докерфайл](https://github.com/Alex-Nosov-ITMO/Clouds_ITMO/blob/main/devops_labs/lab2/scrins/плохой.jpg)


* `FROM ubuntu:latest`
  
    Так как целью нашего контейнера являлась передача скрипта на питоне, подгрузка ОС, так ещё и в версии latest, является ошибочной.
* `RUN apt-get update`
  
    `RUN apt-get install -y python3`
    
    `RUN apt-get install python3-pip -y`

    `RUN pip install matplotlib`

    `RUN pip install numpy`

  Несколько `RUN`, увеличивающие количество слоёв Dockerfile, что существенно замедляет его работу
* `ADD GCD.py ./`
  
  `ADD` вместо `COPY`, их разница состоит в том, что `COPY` более универсальный, может работать с архивами, в отличие от `ADD`
  
* `CMD ["python3", "./GCD.py"]`
  
  Использование CMD вместо ENTRYPOINT, в правилах хорошего тона писать Dockerfile нужно так, чтобы его содержимое было цельным продуктом, не требующим изменений. CMD же эти изменения сделать позволяет.





![Хороший докерфайл](https://github.com/Alex-Nosov-ITMO/Clouds_ITMO/blob/main/devops_labs/lab2/scrins/хороший.jpg)


![Запуск плохого](https://github.com/Alex-Nosov-ITMO/Clouds_ITMO/blob/main/devops_labs/lab2/scrins/запуск%20плохого.jpg)


![Запуск хорошего](https://github.com/Alex-Nosov-ITMO/Clouds_ITMO/blob/main/devops_labs/lab2/scrins/запуск%20хорошего.jpg)

![Наши контейнеры](https://github.com/Alex-Nosov-ITMO/Clouds_ITMO/blob/main/devops_labs/lab2/scrins/контейнеры.jpg)

![Наши образы](https://github.com/Alex-Nosov-ITMO/Clouds_ITMO/blob/main/devops_labs/lab2/scrins/образы.jpg)

![Сборка образа](https://github.com/Alex-Nosov-ITMO/Clouds_ITMO/blob/main/devops_labs/lab2/scrins/сборка.jpg)


