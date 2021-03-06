# Счетчики покрытия тестами

JaCoCo использует набор различных счетчиков для расчета показателей покрытия.

### INSTRUCTION

Наименьшая единица измерения JaCoCo - это инструкции Java-байт-кода. Охват инструкций предоставляет информацию о количестве кода, который был выполнен или пропущен. Этот показатель полностью независим от исходного форматирования и всегда доступен, даже при отсутствии отладочной информации в файлах классов.

### BRANCH

JaCoCo также рассчитывает покрытие филиала для всех ```if``` и ```switch``` операторов. Эта метрика подсчитывает общее количество таких ветвей в методе и определяет количество выполненных или пропущенных веток. Покрытие веток всегда доступно, даже в отсутствие отладочной информации в файлах классов. Обратите внимание, что обработка исключений не рассматривается как ветви в контексте этого определения счетчика.

Если файлы классов не были скомпилированы с отладочной информацией, точки принятия решения могут быть сопоставлены с исходными строками и выделены соответствующим образом:

* Нет покрытия: не было выполнено ни одной ветки в строке (красный ромб)
* Частичное покрытие: была выполнена только часть ветвей в линии (желтый ромб)
* Полный охват: все ветки в линии были выполнены (зеленый бриллиант)


### LINE

Для всех файлов классов, которые были скомпилированы с отладочной информацией, можно рассчитать информацию покрытия для отдельных строк. Строка источника считается выполненной, когда выполнена хотя бы одна инструкция, назначенная этой строке.

В связи с тем, что одна строка обычно компилируется в инструкции из нескольких байт-кода, выделение исходного кода показывает три разных состояния для каждой строки, содержащей исходный код:

* Нет покрытия: в строке не было выполнено никаких инструкций (красный фон)
* Частичное покрытие: была выполнена только часть инструкции в строке (желтый фон)
* Полный охват: все инструкции в строке были выполнены (зеленый фон)