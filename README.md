ConsoleRender
=====================

**ConsoleRender** is a minimalistic class for output to the console.

The main idea of the class and its methods is the back buffer and the screen buffer.
* Back buffer - what needs to be drawn
* Screen buffer - what is now drawn

To provide faster rendering, only the rear buffer cell is drawn that is different from the screen buffer cell. This allows you to reduce the delay between drawing a new "frame".

Cells can differ in three ways:
1. Symbol
2. Symbol Color
3. Background color

The problem of rendering the back buffer is completely different from the screen buffer

Such a problem arises, for example, when it is necessary to fill in a new “frame” with a new color. But if for filling you can cancel the comparison with the screen buffer, and draw directly, then with something difficult and large-scale drawn in a new frame, this will not work. The solution is to turn off the comparison and draw without wasting time. Unfortunately, there is no direct rendering mode yet, so you need to control and implement the output yourself

Planned in the future
1. Direct output mode with correct operation when switching to double buffer mode
2. Switching modes with correct operation
3. Predicting a very different back buffer for rendering without comparing with the screen buffer

---

**ConsoleRender** - минималистичный класс для вывода в консоль.

Основная идея класса и его методов - задний буфер и буфер экрана. 
* Задний буфер - то, что должно быть отрисовано
* Буфер экрана - то, что сейчас нарисовано

Чтобы обеспечить более быструю отрисовку - рисуется лишь та ячейка заднего буфера, что отлична от ячейки буфера экрана. Это позволяет уменьшить задержку между отрисовкой нового "кадра".

Различаться ячейки могут по трем параметрам:

1. Символ
2. Цвет Символа
3. Цвет Фона

#### Проблема отрисовки заднего буфера абсолютно отличного от буфера экрана

Такая проблема возникает, например когда необходимо новый "кадр" залить новым цветом. Но если для заливки можно отменить сравнение с буфером экрана, и отрисовывать напрямую, то с чем-то сложно и масштабно нарисованным в новом кадре это не получится. Решение - отключить сравнение и рисовать не тратя на это время.
*К сожалению, режима прямой отрисовки пока нет, поэтому необходимо самому контролировать и реализовывать вывод*

### В будущем планируется 
1. Режим прямого вывода с корректной работой при переключении в режим двойного буфера
2. Переключение режимов с корректной работой
3. Предугадывание сильно отличающегося заднего буфера для отрисовки без сравнения с буфером экрана
