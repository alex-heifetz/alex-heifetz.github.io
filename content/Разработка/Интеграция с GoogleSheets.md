### Создание проекта

В  [консоли Google Cloud](https://console.cloud.google.com/) необходимо [создать проект](https://console.cloud.google.com/).

![[Pasted image 20231120151817.png|500]]

### Настройка проекта
#### Подключение библиотеки

Для проекта нужно подключить библиотеку для работы с [[GoogleSheets]].

![[Pasted image 20231120151859.png]]

Для этого нужно перейти в меню в [Library](https://console.cloud.google.com/apis/library) , найти в поиске `Google Sheets API` и включить её. 

![[Pasted image 20231120151927.png]]

#### Создание сервисного ключа

Далее нужно вернуться на страницу проекта и перейти в раздел [Credentials](https://console.cloud.google.com/apis/credentials?project=rare-tome-405712).

![[Pasted image 20231120152249.png]]

Далее создаём Ключ сервисного аккаунта

![[Pasted image 20231120152406.png]]

Даём название данному пользователю

![[Pasted image 20231120152747.png]]

Выбираем роль `Владелец` 

![[Pasted image 20231120152820.png]]

Далее необходимо сгенерировать файл ключей для пользователя в **json** формате. 
Для этого переходим в созданного пользователя, далее на вкладку **KEYS** и нажимает кнопку добавления ключа

![[Pasted image 20231120153157.png]]

Выбираем **JSON** ключ

![[Pasted image 20231120153225.png]]

Это будет файл вида: 
```json
{  
  "type": "",  
  "project_id": "",  
  "private_key_id": "",  
  "private_key": "",  
  "client_email": "",  
  "client_id": "",  
  "auth_uri": "",  
  "token_uri": "",  
  "auth_provider_x509_cert_url": "",  
  "client_x509_cert_url": "",  
  "universe_domain": ""  
}
```

Далее для работы с таблицами в документ необходимо дать доступы для нашего сервисного аккаунта, для этого в документе нужно зайти в настройки доступа
![[Pasted image 20231120154102.png]]
и дать доступ по почте взяв значения email из поля `client_email` из **JSON** файла. 