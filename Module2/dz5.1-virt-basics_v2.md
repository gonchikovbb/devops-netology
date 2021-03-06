**Задача 1**
---
<li>
Паравиртуализация - аппаратное обеспечение не моделируется, а гостевое программное обеспечение запускает свои собственные изолированные домены. То есть, гостевые операционные системы подготавливаются для исполнения в виртуализированной среде, для чего их ядро незначительно модифицируется. Операционная система взаимодействует с программой гипервизора, который предоставляет ей гостевой API, вместо использования напрямую таких ресурсов, как таблица страниц памяти. 
Метод паравиртуализации применим лишь в том случае, если гостевые операционные системы имеют открытые исходные коды, которые можно модифицировать согласно лицензии, или же гипервизор и гостевая операционная система разработаны одним производителем с учётом возможности паравиртуализации гостевой системы

<li>Аппара́тная виртуализа́ция — виртуализация с поддержкой специальной процессорной архитектуры. В отличие от программной виртуализации, с помощью данной техники возможно использование изолированных гостевых систем, управляемых гипервизором напрямую.
Гостевая система не зависит от архитектуры хостовой платформы и реализации платформы виртуализации.
Аппаратная виртуализация обеспечивает производительность, сравнимую с производительностью невиртуализованной машины, что дает виртуализации возможность практического использования и влечет её широкое распространение. Наиболее распространены технологии виртуализации Intel-VT и AMD-V.

<li>Виртуализация на уровне ОС
Контейнерная виртуализация — виртуализация на уровне операционной системы — позволяет запускать изолированные виртуальные системы на одном физическом узле, но не позволяет запускать операционные системы с ядрами, отличными от типа ядра базовой операционной системы. При таком подходе не существует отдельного слоя гипервизора, вместо этого сама хостовая операционная система отвечает за разделение аппаратных ресурсов между несколькими гостевыми системами (контейнерами) и обеспечивает их независимость. Некоторые реализации — FreeBSD Jail (2000), Virtuozzo Containers (2000), Solaris Containers (2005), Linux-VServer[en], OpenVZ (2005), LXC (2008), iCore Virtual Accounts (2008), Docker (2013).

**Задача 2**
---
Условия использования:
<li>Высоконагруженная база данных, чувствительная к отказу – Приоритетней будет использование физических серверов, так как на «голых железках» не будет отказов таких как на виртуальных машинах. 
<li>Различные Java-приложения – Виртуализация уровня ОС. Можно, в рамках одной виртуальной машины развернуть необходимое количество контейнеров, которые будут изолированы друг от друга
<li>Windows системы для использования Бухгалтерским отделом - физический сервер. Для бухгалтерского отдела с Windows, можно поставить просто физические сервер.
<li>Системы, выполняющие высокопроизводительные расчеты на GPU – Паравиртуализация, позволяет добиться более высокой производительности, так как гипервизор частично игнорируется за счет модифицированных ОС, что позволяет не тратить ресурсы и время.

**Задача 3**
---
Xen — монитор виртуальных машин (VMM), или гипервизор. Работает в паравиртуальном режиме и в режиме аппаратной виртуализации (HVM), использует аппаратные возможности процессоров, поэтому не имеет привязки к конкретной операционной системе и может быть установлен «поверх» только лишь аппаратного обеспечения, в так называемом режиме bare metal. Способен поддерживать одновременную работу большого числа виртуальных машин на одной физической, при этом не тратя значительных вычислительных ресурсов.

***Какие режимы виртуализации работают у Xen одновременно?
Все вами перечисленные?***

Xen поставляется в двух вариациях, и может работать одновременно на том же физическом хосте в режиме Xen PV (паравиртуализация) и HVM (полная аппаратная виртуализация)

