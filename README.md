# devops-netology

.gitignore в каталоге terrafrom нацелен на игнорирование различных временных и конфиденциальных файлов, которые не должны попадать в систему контроля версий при работе с Terraform. 

Описание

Каталог .terraform: Весь его содержимое будет проигнорировано, так как он содержит временные файлы, которые Terraform создает для работы.

Файлы состояния .tfstate: Эти файлы отслеживают текущее состояние инфраструктуры, управляемой Terraform. Они могут содержать чувствительные данные, такие как пароли и ключи доступа, поэтому их игнорируют.

Файлы с логами ошибок (crash logs): Логи аварийных завершений работы Terraform (crash.log и другие файлы с префиксом crash.), которые не нужны в репозитории, будут проигнорированы.

Файлы с переменными .tfvars: Эти файлы могут содержать чувствительные данные, например, пароли или секретные ключи, поэтому их исключают из системы контроля версий.

Файлы переопределений (override files): Эти файлы используются для локальных переопределений ресурсов, которые не должны быть сохранены в репозитории, так как они специфичны для конкретных окружений.

Временные файлы блокировок .terraform.tfstate.lock.info: Эти файлы создаются при выполнении команды terraform apply для предотвращения конфликтов при одновременном изменении инфраструктуры.

Конфигурационные файлы CLI (.terraformrc, terraform.rc): Эти файлы содержат пользовательские настройки командной строки Terraform и не нужны в репозитории.

