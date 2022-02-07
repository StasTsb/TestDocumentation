<!DOCTYPE html>
<h1>Optimization of Graphics and Assets</h1>

<table class="demoTable" style="height: 623px;">
<tbody>
<tr style="height: 17px;">
<td style="width: 672.438px; height: 17px;" colspan="5">Работа с камерой</td>
</tr>
<tr style="height: 17px;">
<td style="width: 258.112px; height: 17px;">Чем больше камер, тем выше нагрузка на CPU</td>
<td><img src="https://github.com/StasTsb/TestDocumentation/blob/master/ScreenOpti/3.png" width="340" height="126"></td>
</tr>
<tr style="height: 17px;">
<td style="width: 258.112px; height: 17px;">Использование пост обработки увеличивает нагрузку на GPU</td>
<td style="width: 258.112px; height: 17px;">O_O </td>
</tr>
<tr style="height: 17px;">
<td style="width: 258.112px; height: 17px;">MSAA не выше 4Х на любых мобильных платформах</td>
<td style="width: 258.112px; height: 17px;">O_O </td>
</tr>
<tr style="height: 17px;">
<td style="width: 258.112px; height: 17px;">Используем Forward-режим рендеринга без использования HDR<br> Снижаем нагрузку на GPU</td>
<td style="width: 258.112px; height: 17px;">O_O </td>
</tr>
<tr style="height: 17px;">
<td style="width: 258.112px; height: 17px;">Выставляем на камере Clear Flags<br> Указываем что нужно очищать при рендеренге каждый кадр</td>
<td style="width: 258.112px; height: 17px;">O_O </td>
</tr>
<tr style="height: 17px;">
<td style="width: 258.112px; height: 17px;">Настраиваем допустимый Clipping Planes при разработке 3D<br> Ограничиваем область прорисовки дальних обьектов</td>
<td style="width: 258.112px; height: 17px;">O_O </td>
</tr>
<tr style="height: 17px;">
<td style="width: 672.438px; height: 17px;" colspan="5">Работа с рендерингом</td>
</tr>
<tr style="height: 17px;">
<td style="width: 258.112px; height: 17px;">Используем облегченные API (Vulkan или Metal)<br> Для 2D достаточно (OpenGL2)</td>
<td style="width: 258.112px; height: 17px;">O_O </td>
</tr>
</tr>
<tr style="height: 17px;">
<td style="width: 258.112px; height: 17px;">Используем Occlusion Culling<br> Для выгрузки обьектов вне поля зрения</td>
<td style="width: 258.112px; height: 17px;">O_O </td>
</tr>
</tr>
<tr style="height: 17px;">
<td style="width: 258.112px; height: 17px;">Используем только запеченное освещение<br> Отказываемся от теней и Reflection Probes <br> Realtime расчеты не используем вовсе</td>
<td style="width: 258.112px; height: 17px;">O_O </td>
</tr>
</tr>
<tr style="height: 17px;">
<td style="width: 258.112px; height: 17px;">Стараемся использовать Static и Dynamic Batching для обьектов и объединения геометрии</td>
<td style="width: 258.112px; height: 17px;">O_O </td>
</tr>
</tr>
<tr style="height: 17px;">
<td style="width: 258.112px; height: 17px;">Стараемся не использовать процедурные системы частиц</td>
<td style="width: 258.112px; height: 17px;">O_O </td>
</tr>
</tr>
<tr style="height: 17px;">
<td style="width: 258.112px; height: 17px;">Анимацию юзаем по минимуму<br> Где возможно анимируем через скрипты или DOTween </td>
<td style="width: 258.112px; height: 17px;">O_O </td>
</tr>
</tr>
<tr style="height: 17px;">
<td style="width: 258.112px; height: 17px;">По возможности устанавливаем значение флага "Realtime Pixel Lights" на 0 </td>
<td style="width: 258.112px; height: 17px;">O_O </td>
</tr>
</tr>
<tr style="height: 17px;">
<td style="width: 258.112px; height: 17px;">Выключаем Soft Particles</td>
<td style="width: 258.112px; height: 17px;">O_O </td>
</tr>
</tr>
<tr style="height: 17px;">
<td style="width: 258.112px; height: 17px;">Стараемся использовать простые шейдера с минимальным количеством инструкций</td>
<td style="width: 258.112px; height: 17px;">O_O </td>
</tr>
</tr>
<tr style="height: 17px;">
<td style="width: 258.112px; height: 17px;">Избегаем сэмплинга в Reflection Probes</td>
<td style="width: 258.112px; height: 17px;">O_O </td>
</tr>
</tr>
<tr style="height: 17px;">
<td style="width: 258.112px; height: 17px;">Используем общий материал для объектов</td>
<td style="width: 258.112px; height: 17px;">O_O </td>
</tr>
</tr>
<tr style="height: 17px;">
<td style="width: 258.112px; height: 17px;">Используем Gamma рендеринг вместо Linear</td>
<td style="width: 258.112px; height: 17px;">O_O </td>
</tr>
</tr>
<tr style="height: 17px;">
<td style="width: 258.112px; height: 17px;">Стараемся использовать URP-рендеринг вместо Legacy (Built-in)</td>
<td style="width: 258.112px; height: 17px;">O_O </td>
</tr>
</tr>
<tr style="height: 17px;">
<td style="width: 258.112px; height: 17px;">Изучить и использовать ShaderVariants<br> Для уменьшения нагрузки на GPU</td>
<td style="width: 258.112px; height: 17px;">O_O </td>
</tr>
</tr>
<tr style="height: 17px;">
<td style="width: 258.112px; height: 17px;">При добавлении/ удалении шейдеров в проекте, держим актуальным список Always Inculded Shaders</td>
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