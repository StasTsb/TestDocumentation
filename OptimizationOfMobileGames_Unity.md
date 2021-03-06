<!DOCTYPE html>
<h1>Optimization of Graphics and Assets</h1>

<table class="demoTable" style="height: 623px;">
<tbody>
<tr style="height: 17px;">
<td style="width: 672.438px; height: 17px;" colspan="5">1. Работа с камерой</td>
</tr>
<tr style="height: 17px;">
<td style="width: 258.112px; height: 17px;">1.1 Чем больше камер, тем выше нагрузка на CPU</td>
<td><img src="https://github.com/StasTsb/TestDocumentation/blob/master/ScreenOpti/1.png" width="340" height="126"></td>
</tr>
<tr style="height: 17px;">
<td style="width: 258.112px; height: 17px;">1.2 Использование пост обработки увеличивает нагрузку на GPU</td>
<td style="width: 258.112px; height: 17px;">O_O </td>
</tr>
<tr style="height: 17px;">
<td style="width: 258.112px; height: 17px;">1.3 MSAA не выше 4Х на любых мобильных платформах</td>
<td><img src="https://github.com/StasTsb/TestDocumentation/blob/master/ScreenOpti/3.png" width="340" height="126"></td>
</tr>
<tr style="height: 17px;">
<td style="width: 258.112px; height: 17px;">1.4 Используем Forward-режим рендеринга без использования HDR<br> Снижаем нагрузку на GPU</td>
<td><img src="https://github.com/StasTsb/TestDocumentation/blob/master/ScreenOpti/4.png" width="340" height="126"></td>
</tr>
<tr style="height: 17px;">
<td style="width: 258.112px; height: 17px;">1.5 Выставляем на камере Clear Flags<br> Указываем что нужно очищать при рендеренге каждый кадр</td>
<td><img src="https://github.com/StasTsb/TestDocumentation/blob/master/ScreenOpti/5.png" width="340" height="126"></td>
</tr>
<tr style="height: 17px;">
<td style="width: 258.112px; height: 17px;">1.6 Настраиваем допустимый Clipping Planes при разработке 3D<br> Ограничиваем область прорисовки дальних обьектов</td>
<td><img src="https://github.com/StasTsb/TestDocumentation/blob/master/ScreenOpti/6.png" width="340" height="126"></td>
</tr>
<tr style="height: 17px;">
<td style="width: 672.438px; height: 17px;" colspan="5">2. Работа с рендерингом</td>
</tr>
<tr style="height: 17px;">
<td style="width: 258.112px; height: 17px;">2.1 Используем облегченные API (Vulkan или Metal)<br> Для 2D достаточно (OpenGL2)</td>
<td><img src="https://github.com/StasTsb/TestDocumentation/blob/master/ScreenOpti/7.png" width="340" height="126"></td>
</tr>
</tr>
<tr style="height: 17px;">
<td style="width: 258.112px; height: 17px;">2.2 Используем Occlusion Culling<br> Для выгрузки обьектов вне поля зрения</td>
<td><img src="https://github.com/StasTsb/TestDocumentation/blob/master/ScreenOpti/8.png" width="340" height="126"></td>
</tr>
</tr>
<tr style="height: 17px;">
<td style="width: 258.112px; height: 17px;">2.3 Используем только запеченное освещение<br> Отказываемся от теней и Reflection Probes <br> Realtime расчеты не используем вовсе</td>
<td style="width: 258.112px; height: 17px;">O_O </td>
</tr>
</tr>
<tr style="height: 17px;">
<td style="width: 258.112px; height: 17px;">2.4 Стараемся использовать Static и Dynamic Batching для обьектов и объединения геометрии</td>
<td><img src="https://github.com/StasTsb/TestDocumentation/blob/master/ScreenOpti/10.png" width="340" height="126"></td>
</tr>
</tr>
<tr style="height: 17px;">
<td style="width: 258.112px; height: 17px;">2.5 Стараемся не использовать процедурные системы частиц</td>
<td style="width: 258.112px; height: 17px;">O_O </td>
</tr>
</tr>
<tr style="height: 17px;">
<td style="width: 258.112px; height: 17px;">2.6 Анимацию юзаем по минимуму<br> Где возможно анимируем через скрипты или DOTween </td>
<td style="width: 258.112px; height: 17px;">O_O </td>
</tr>
</tr>
<tr style="height: 17px;">
<td style="width: 258.112px; height: 17px;">2.7 По возможности устанавливаем значение флага "Realtime Pixel Lights" на 0 </td>
<td style="width: 258.112px; height: 17px;">O_O </td>
</tr>
</tr>
<tr style="height: 17px;">
<td style="width: 258.112px; height: 17px;">2.8 Выключаем Soft Particles</td>
<td style="width: 258.112px; height: 17px;">O_O </td>
</tr>
</tr>
<tr style="height: 17px;">
<td style="width: 258.112px; height: 17px;">2.9 Стараемся использовать простые шейдера с минимальным количеством инструкций</td>
<td style="width: 258.112px; height: 17px;">O_O </td>
</tr>
</tr>
<tr style="height: 17px;">
<td style="width: 258.112px; height: 17px;">2.10 Избегаем сэмплинга в Reflection Probes</td>
<td style="width: 258.112px; height: 17px;">O_O </td>
</tr>
</tr>
<tr style="height: 17px;">
<td style="width: 258.112px; height: 17px;">2.11 Используем общий материал для объектов</td>
<td style="width: 258.112px; height: 17px;">O_O </td>
</tr>
</tr>
<tr style="height: 17px;">
<td style="width: 258.112px; height: 17px;">2.12 Используем Gamma рендеринг вместо Linear</td>
<td style="width: 258.112px; height: 17px;">O_O </td>
</tr>
</tr>
<tr style="height: 17px;">
<td style="width: 258.112px; height: 17px;">2.13 Стараемся использовать URP-рендеринг вместо Legacy (Built-in)</td>
<td style="width: 258.112px; height: 17px;">O_O </td>
</tr>
</tr>
<tr style="height: 17px;">
<td style="width: 258.112px; height: 17px;">2.14 Изучить и использовать ShaderVariants<br> Для уменьшения нагрузки на GPU</td>
<td style="width: 258.112px; height: 17px;">O_O </td>
</tr>
</tr>
<tr style="height: 17px;">
<td style="width: 258.112px; height: 17px;">2.15 При добавлении/ удалении шейдеров в проекте, держим актуальным список Always Inculded Shaders</td>
<td style="width: 258.112px; height: 17px;">O_O </td>
</tr>
</tr>
<tr style="height: 17px;">
<td style="width: 258.112px; height: 17px;">В некоторых случаях необходимо разогреть видео-чип перед стартом игры(инициализируя обьекты на сцене Preload)<br> Для исключения микро-фризов при первой отрисовке объекта</td>
<td style="width: 258.112px; height: 17px;">O_O </td>
</tr>
<tr style="height: 17px;">
<td style="width: 672.438px; height: 17px;" colspan="5">Работа с ресурсами</td>
</tr>

</tr>
</tbody>
</table>
<p></p>
