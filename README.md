# LPC Sound Codec Lab

Экспериментальная браузерная лаборатория для сравнения параметрических и стандартных аудиокодеков, а также потоковый декодер `LPC2 Improved` для ATmega328P.

**Онлайн-версия:** [witali.github.io/LPC-sound-codec](https://witali.github.io/LPC-sound-codec/)

## Состав проекта

- [`index.html`](index.html) — актуальная автономная веб-страница. Она содержит LFA-3, LPC1, LPC2 Improved, Ogg Vorbis и Opus.
- [`arduino/Lpc2AvrDecoder`](arduino/Lpc2AvrDecoder) — библиотека декодирования LPC2 для Arduino Uno/Nano, примеры SD и PROGMEM, конвертер `.lp2` в заголовок C++.
- [`archive/web`](archive/web) — все промежуточные HTML-версии, выгруженные из исходного чата.
- [`docs`](docs) — перенесённая и систематизированная документация из обсуждения.

## Быстрый старт

Откройте `index.html` в современном браузере, загрузите аудиофайл и выберите кодек. Экспериментальные LFA/LPC-режимы работают локально. Для первой загрузки WASM-кодировщика Ogg Vorbis нужен интернет.

Рекомендуемый профиль LPC2 для ATmega328P:

```text
кодек:          LPC2 Improved
частота:        8 кГц
шаг кадров:     20 мс
окно анализа:   32 мс
LPC order:      10
предыскажение:  около 0,85
```

Для Arduino см. [`arduino/Lpc2AvrDecoder/README_RU.md`](arduino/Lpc2AvrDecoder/README_RU.md).

## Документация

- [Архитектура и эволюция кодеков](docs/codec-design.md)
- [Веб-лаборатория и форматы файлов](docs/web-lab.md)
- [Ограничения ATmega328P и выбор кодека](docs/atmega-audio.md)
- [Речевые кодеки мобильной связи](docs/mobile-codecs.md)
- [Хронология разработки](docs/development-history.md)

Источник материалов — [опубликованная переписка ChatGPT](https://chatgpt.com/share/6a6ccb0d-434c-83ed-88b4-2ced1b7dc701).
