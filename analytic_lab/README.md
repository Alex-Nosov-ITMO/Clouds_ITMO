# Аналитические лабы

## **AWS**

### Состав команды:
Кальянная №46:
+ Носов Александр (К3222)
+ Телунц Эдуард (К3221)
+ Шестаков Максим (К3221)
+ Будунов Будун (К3241)

### **Цель работы**:


Знакомство с облачными сервисами. Понимание уровней абстракции над инфраструктурой в облаке. Формирование понимания типов потребления сервисов в сервисной-модели. Сопоставление сервисов между разными провайдерами. Оценка возможностей миграции на отечественные сервисы.


### **Дано**:


Слепок данных биллинга от провайдера после небольшой обработки в виде SQL-параметров. Необходимо заполнить пустые ячейки с заголовками IT Tower, Service Family, Service Type, Service Sub-Type, используя элементы модели Apptio TBM Unified Model (ATUM) для упрощения соответствия сервисов. Определить соответствие каждого сервиса международного провайдера русскому сервису.


### **Необходимо**:

``` 
1. Импортировать файл .csv в Excel или любую другую программу работы с таблицами.
2. Выполнить описание каждого сервиса AWS.
3. Определить соответствие каждого сервиса международного провайдера русскому сервису.
```

### **Начальные данные**:

<img width="468" alt="image" src="https://github.com/Alex-Nosov-ITMO/Clouds_ITMO/blob/main/analytic_lab/scrins/begAWS1.jpg">

<img width="468" alt="image" src="https://github.com/Alex-Nosov-ITMO/Clouds_ITMO/blob/main/analytic_lab/scrins/begAWS2.jpg">

### **Анализ сервисов AWS**:

**1. Amazon EC2**\
Amazon EC2 - это сервис для аренды виртуального компьютера в облаке, плюсом на этой ВМ можно запускать своё ПО, масштабировать ресурсы (например, доарендовать ещё ВМ для увеличения мощности/памяти). Помимо этого мы получаем плюсы использования облачных технологий в виде высокой безопасности сервера.

**Amazon DAX**\
Amazon DAX - это ускоритель для сервиса Amazon DynamoDB. Суть его работы заключается в том, что он кэширует запросы и ответы базы данных, за счёт чего производительность вырастает в разы (т.к. они запросы считаются единожды и потом достаётся их результат). Ускоритель легко поддаётся масштабируемости, легко внедряется (не требует больших изменений в коде), помимо этого ещё и поддерживает высокую безопасность с помощью IAM (менеджер управления доступом).

**Amazon Dynamo DB**\
Amazon Dynamo DB – это управляемая нереляционная БД, нужная для того, чтобы запускать высокопроизводительные масштабируемые приложения. Основными характеристиками Amazon Dynamo DB являются: достаточно хорошая доступность и надежность, отличное масштабирование базы данных, соответствующая реализация безопасности

**AWS Database Migration Svc**\
AWS DMS - сервис для миграции данных из разных источников, поддерживает работу с облачными хранилищами и разными типами БД. Из особенностей можно выделить поддержку работы в режиме реального времени, а также безопасность за счёт шифрования данных. По сути нужен для переноса данных между различными хранилищами.

**AWS Device Farm**\
AWS Device Farm - грубо говоря песочница для тестирования мобильных приложений в различных реальных условиях. Можно регулировать количество тестируемых устройств, платформы, на которых они работают, писать тесты самостоятельно (ручные и автоматизированные). Опять же сервис безопасен, также он предоставляет подробные отчёты о своих результатах.

**AWS IoT Device Managemenе**\
AWS IoT Device Management – это сервис, помогающий со структуризацией, регистрацией, постоянным мониторингом и удаленным управлением устройств в IoT. Основные характеристики: безопасный удаленный мониторинг состояния, выполнение действий в реальном времени, быстрое подключение и организация собственных устройств

**APNFee**\
APNFee - плата за партнёрство с Amazon Partner Network. Стоит 2500 долларов, предоставляет разные уровни партнёрства. Больше сказать особо нечего..

**AWS Translate**\
AWS Translate – это сервис, который занимается переводом текстов, статей, делает это он с помощью методов Machine Learning, а точнее его подраздела Deep Learning. Перевод осуществляется с помощью нейросетей, поэтому он такой точный и достаточно быстрый.

**AWS Transcribe**\
AWS Transcribe – это сервис, который занимается распознаванием речи, которое осуществляется посредством применения методов Deep Learning. Характеристики: поддержка разных языков и диалектов, применяется для создания различных субтитров, анализа аудиозаписей. Распознование речи и подобные операции осуществляются с помощью использования нейросетей

**AWS CloudHSM**\
AWS CloudHSM – это сервис, позволяющий использовать специальные аппаратные модули безопасности. Выделим основные характеристики: возможность защиты созданных криптографических ключей на FIPS-подтвержденных аппаратных устройствах, обеспечение безопасного хранения и обработки данных, облегчение обработки SSL для веб-сервисов, хранение ключей для TDE в БД Oracle

**Amazon CodeBuild**\
Amazon CodeBuild - сервис для автоматизации сборки в облаке, поддерживает разные ЯП, масштабирование (за счёт использования нескольких ВМ параллельно), даёт возможность протестить  программы на локальной машине. Если кратко, то данный сервис предоставляет необходимые для эффективных сборки и тестирования приложений.

**Amazon Comprehend**\
Amazon Comprehend - это служба обработки естественного языка(NLP) в облаке AWS. На сервере можно анализировать текст, выделять ключевую информацию, классифицировать текст. Также можно определять настроение (положительное, отрицательное, нейтральное) и языковые элементы в текстовых данных. Сервис позволяет анализировать неструктурированные данные и определять именованные сущности. Также возможна легкая интеграция с другими сервисами, такими как Amazon S3, AWS Lamda и другие.

**Amazon Comprehend Medical**\
Amazon Comprehend Medical - это также служба обработки естественного языка(NLP). Но в отличие от Amazon Comprehend она разработана для анализа медицинских текстов и извлечения из них структурированных данных из медицинских документов. Сервис выявляет ключевые понятия и сущности, а также отношения в текстах, которые помогают при исследованиях и анализе данных.

**AWS Backup**\
AWS Backup - это сервис резервного копирования. в котором можно создавать и управлять резервными копиями данных проектов и приложений с облачных сервисах AWS. Сервис позволяет определять политики хранения данных, то есть управлять тем, как долго хранить данные и когда их можно удалять. Также сервис обеспечивает возможность создавать резервные копии данных других AWS сервисов, например Amazon DynamoDB,  Amazon EBS и другие.


### **Маппинг AWS сервисов с российскими аналогами**:

| AWS | Yandex | Ссылка на описание рос. сервиса
  |---|---------------|-------|
  | AmazonEC2 |Yandex Compute Cloud|(https://cloud.yandex.ru/docs/compute/)|
  | AmazonDAX |-|-|
  | AmazonDynamoDB |Yandex Managed Service for YDB|(https://cloud.yandex.ru/docs/ydb/)|
  | AWSDatabaseMigrationSvc |Yandex Data Transfer|https://cloud.yandex.ru/docs/data-transfer/|
  |AWSDeviceFarm|Yandex Load Testing|(https://cloud.yandex.ru/docs/load-testing/)|
  |IoTDeviceManagement|Yandex IoT Core|https://cloud.yandex.ru/services/iot-core|
  |APNFee|-|-|
  |translate|Yandex Translate|(https://cloud.yandex.ru/docs/translate/)|
  |transcribe|Yandex SpeechKit|(https://cloud.yandex.com/en/docs/speechkit/)|
  |CloudHSM|Yandex Key Management Service|(https://cloud.yandex.ru/docs/kms/concepts/hsm)|
  |CodeBuild|-|-|
  |comprehend|Yandex SpeechKit|(https://cloud.yandex.ru/services/speechkit)|
  |comprehendmedical|Облачные решения для здравоохранения|(https://cloud.yandex.ru/solutions/healthcare)|
  |AWSBackup|Yandex.Backup|(https://cloud.yandex.ru/services/backup)|





### **Итоговая таблица**:

<img width="468" alt="image" src="https://github.com/Alex-Nosov-ITMO/Clouds_ITMO/blob/main/analytic_lab/scrins/endAWS1.jpg">

<img width="468" alt="image" src="https://github.com/Alex-Nosov-ITMO/Clouds_ITMO/blob/main/analytic_lab/scrins/endAWS2.jpg">



## **Вывод**

В ходе аналитической лабараторной работы было осуществлено знакомство с облачными сервисами AWS, а также было провелено сравнение с российсими сервисами.

Проанализировав таблицу, можно сделать вывод, что для сервисов AWS существуют аналоги в Yandex Cloud, однако функционал некоторых из этих сервисов является более обобщенным. Так, некоторые сервисы из Yandex Cloud могут заменять два или более сервисов Azure.





## **Azure**

### Состав команды:
Кальянная №46:
+ Носов Александр (К3222)
+ Телунц Эдуард (К3221)
+ Шестаков Максим (К3221)
+ Будунов Будун (К3241)

### **Цель работы**:


Знакомство с облачными сервисами. Понимание уровней абстракции над инфраструктурой в облаке. Формирование понимания типов потребления сервисов в сервисной-модели. Сопоставление сервисов между разными провайдерами. Оценка возможностей миграции на отечественные сервисы.


### Дано:


Слепок данных биллинга от провайдера после небольшой обработки в виде SQL-параметров. Необходимо заполнить пустые ячейки с заголовками IT Tower, Service Family, Service Type, Service Sub-Type, используя элементы модели Apptio TBM Unified Model (ATUM) для упрощения соответствия сервисов. Определить соответствие каждого сервиса международного провайдера русскому сервису.


### **Необходимо**:

``` 
1. Импортировать файл .csv в Excel или любую другую программу работы с таблицами.
2. Выполнить описание каждого сервиса Azure.
3. Определить соответствие каждого сервиса международного провайдера русскому сервису.
```

### **Начальные данные**:

<img width="468" alt="image" src="https://github.com/Alex-Nosov-ITMO/Clouds_ITMO/blob/main/analytic_lab/scrins/begAzure.jpg">

### **Анализ сервисов Azure**:

**Azure Data Management**\
Azure Data Management – это сервис, который предоставляет специальные инструменты для того, чтобы управлять и обрабатывать данные. Перечислим основные характеристики, присущие .тому сервису: Обрабатывать данные возможно с помощью достаточно мощных инструментов: Azure Data Factory, Azure Databricks, Azure Stream Analytics. Данные можно хранить с помощью сервисов хранения: Azure  Blob Storage,  Azure  Azure Data Lake Storage,  Azure SQL Database. Простой поиск, обеспеченный сервисом Azure Data Catalog. Безопасный обмен данными с помощью сервиса:  Azure Data Share

**Azure Machine Learning Studio**\
Azure Machine Learning Studio – это сервис, являющийся IDE, основанной на графическом интерфейсе для того, чтобы создавать и эксплуатировать различные решения задач машинного обучения. Благодаря данному сервису можно использовать уже готовые решения для задач машинного обучения, либо же создавать собственные

**Azure Bastion**\
Azure Bastion - сервис для безопасного доступа к виртуальным машинам, с его помощью можно перестать использовать общедоступные порты. Bastion использует RDP-протокол (удалённого доступа), SSH и Azure Portal (для единого доступа к управлению инфраструктурой) для доступа к ВМ.

**Azure API Management**\
Azure API Management - сервис который позволяет компаниям работать с API. Позволяет создавать и документировать API с использованием виртуального дизайнера, при помощи него легко публиковать и управлять API за счет контроля версий, возможна работа с разными протоколами, обеспечивает масштабируемость.

**Azure Monitor**\
Azure Monitor - это служба мониторинга и аналитики в облаке. Она предоставляет возможность отслеживать состояние и производительность ресурсов в облаке. Аzure Monitor собирает и хранит логи и данные метрик о работе ресурсов, позволяет настроить оповещения при определенных условиях, предоставляет средства для диагностики и трассировки приложений, обеспечивает обнаружение угроз и безопасность инфраструктуры. Также интегрируется с другими сервисами Azure, такими как AKS и Application Insights.

**Azure Backup**\
Azure Backup - сервис для резервного копирования (РК), из характеристик можно отметить поддержку РК виртуальных машин, работающих на Azure, также поддержку копирования различных БД, копии серверов и приложений, не связанных с Azure (если они интегрированы с Azure Backup Agent). Интересной фичей является "гранулированное восстановление" , т.е. бэкап может восстанавливать не все данные целиком, а на уровне файла, папки, приложения и т.д. Это позволяет не копировать лишние данные, которые уже не пригодятся. Можно настраивать периодичность РК, также данные шифруются, благодаря чему безопасность копирования высокая.

**Azure Business Analytics**\
Azure Business Analytics - сервис для анализа данных и бизнес-аналитики. Он позволяет визуализировать данные для выявления в них информации. Для анализа данных и создания отчётов можно также использовать Power BI, ещё один сервис от Microsoft для совместной работы по бизнес-проектам.

**Azure Virtual Machines**\
Azure Virtual Machines - это сервис, который позволяет создавать и управлять виртуальными машинами в облаке, а не на своем железе. Также позволяет использовать готовые образы виртуалок, чтобы быстро разворачивать приложения. Также этот сервис можно использовать для тестирования и разработки приложений.   Azure Virtual Machines License Included - это вариант включения себя в лицензию. Она распространяется на ОС и другое ПО. Вы оплачиваете только стоимость ВМ.


### **Маппинг Azure сервисов с российскими аналогами**:

| Azure | Yandex | Ссылка на описание рос. сервиса
  |---|---------------|-------|
  |Azure Data Management|Yandex DataSphere, Yandex Data Transfer|https://cloud.yandex.ru/docs/datasphere/, https://cloud.yandex.ru/docs/data-transfer/|
  |Azure Machine Learning Studio|Yandex DataSphere|https://cloud.yandex.ru/docs/datasphere/|
  |Azure Bastion|Compute Cloud|https://cloud.yandex.ru/docs/compute/|
  |Azure API Management|Yandex API Gateway|https://cloud.yandex.ru/docs/api-gateway/|
  |Azure Monitor|Yandex Monitoring|https://cloud.yandex.ru/docs/monitoring/|
  |Azure Backup|Yandex.Backup|https://cloud.yandex.ru/services/backup|
  |Azure Business Analytics|Yandex DataLens|https://cloud.yandex.ru/docs/datalens/|
  |Azure Virtual Machines|Yandex ComputeClouf|https://cloud.yandex.ru/docs/compute/|
  



## **Вывод**

В ходе аналитической лабараторной работы было осуществлено знакомство с облачными сервисами Azure, а также было провелено сравнение с российсими сервисами.

Проанализировав таблицу, можно сделать вывод, что для сервисов Microsoft Azure существуют аналоги в Yandex Cloud, однако функционал некоторых из этих сервисов является более обобщенным. Так, некоторые сервисы из Yandex Cloud могут заменять два или более сервисов Azure.





# **Теоритические вопросы**

### Состав команды:
Кальянная №46:
+ Носов Александр (К3222)
+ Телунц Эдуард (К3221)
+ Шестаков Максим (К3221)
+ Будунов Будун (К3241)

## **Вопрос 1**:

Безопасно ли хранить данные в публичном облаке? Опишите ситуацию, когда так делать можно, а когда нельзя?


Безопасно ли хранить данные в публичном облаке (ПО)? Опишите ситуацию, когда так делать можно, а когда нельзя? 
Как следует из формулировки вопроса, безопасность хранения данных в публичном облаке зависит от конкретных факторов.

Например, если облако хорошо защищено, данные в нём шифруются, есть системы мониторинга безопасности, облако соответствует различным стандартам безопасности, его защищённость регулярно проверяют и отслеживают уязвимые моменты - то да, хранить данные в нём безопасно. В различные мониторинги так же входят и отслеживание действий пользователей, различных вредоносных вторжений, их анализ. 

Так же для надёжной безопасности облако должно поддерживать систему резервного копирования (Backup), чтобы утерянные данные можно было восстановить. Потеря данных тоже может быть различной степени критичности, если, например, данные конфиденциальны и запрещены к общественному показу, то лучше использовать иную форму хранения данных, а если их попадание в сеть не страшно и есть система бэкапа - то вполне себе безопасно и надёжно.

В заключение ответа на этот вопрос хочется добавить, что для надёжного хранения данных в публичном облаке необходимо грамотно настраивать систему доступа, чтобы каждый уровень доступа был защищён своей системой шифрования. Если организация, желающая хранить данные в ПО не готова настраивать систему под требования безопасного хранения или же не готова тратиться на облачные сервисы, поддерживающие стандарты безопасности, то в этом случае их данные лучше там не хранить.





## **Вопрос 2**:


Для чего введен термин Infrastructure as a Code? Какие выгоды это несет с точки зрения автоматизации, безопасности? Предложите набор компонентов, которые нужно использовать при развертывании инфраструктуры как кода.


Инфраструктура как код (IaC) — это метод для настройки и управления инфраструктурой кодом, вместо того, чтобы настраивать всю инфраструктуру вручную или же с помощью графических интерфейсов. Перечислим плюсы такого подхода: IaC предоставляет возможность для автоматизации процесса развертывания и управления инфраструктурой, что снижает количество ошибок, которые допускаются человеком при ручной настройке. Есть ряд компонент, использующиеся при такой методологии. При написании кода используются языки: Terraform, Ansible. Система контроля версий для кода - git. Контейнеризация — например Docker контейнеры для упаковки и доставки приложений вместе с их зависимостями. Также необходимо упомянуть о CI/CD, для этой компоненты используются такие инструменты как: GitLab CI/CD, Jenkins. Также необходима такая компонента как мониторинг и логирование для того, чтобы отслеживать работу инфраструктуру — Prometheus – это отличный выбор



