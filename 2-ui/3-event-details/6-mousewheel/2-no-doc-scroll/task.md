# Прокрутка без влияния на страницу

[importance 4]

В большинстве браузеров если в процессе прокрутки `textarea` колёсиком мышки (или жестами) мы достигаем границы элемента, то прокрутка продолжается уже на уровне страницы (в Firefox при этом будет небольшая задержка перед продолжением прокрутки).

Иными словами, если в примере ниже вы попробуете прокрутить `textarea` вниз, то когда прокрутка дойдёт до конца -- начнёт прокручиваться документ:

[iframe src="source" border="1" height=300]

То же самое происходит при прокрутке вверх.

В интерфейсах редактирования, когда большая `textarea` является основным элементом страницы, такое поведение может быть неудобно. 

Для редакторования более оптимально, чтобы при прокрутке до конца `textarea` страница не "улетала" вверх и вниз.

Вот тот же документ, но с желаемым поведением `textarea`:

[iframe src="solution" border="1" height=300]

Задача: 
<ul>
<li>Создать скрипт, который при подключении к документу исправлял бы поведение всех `textarea`, чтобы при прокрутке они не трогали документ.</li>
<li>Направление прокрутки -- только вверх или вниз.</li>
<li>Редактор прокручивает только мышкой или жестами (на мобильных устройствах), прокрутку клавиатурой здесь рассматривать не нужно (хотя это и возможно).</li>
</ul>

