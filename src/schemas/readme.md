# Схемы данных

Представлены в нотации `typegoose`. Для схем данных характерна проблема циклических зависимостей,
особенно при использовании внутри конструкций вида `import { models } from "models"` (которые характерны
для больших схем данных, опирающихся друг на друга).

Схемы могут представлять собой большие логические классы, описывающие как структуру данных документов, так и логику
обработки данных в них, используя собственные и статические методы. Возможно использование обращений к другим
моделям данных для получения промежуточных результатов и накопления сложных отчетов.

Схемы являются предельно низким уровнем логики данных, и не должны обращаться к контроллерам и контекстным им данным.
В общем случае в методах схем данных могут использоваться обращения к сокетам, наличие данных в которых повлияет 

В контроллеры и вне