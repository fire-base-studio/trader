# trader
Экспериментальный трейдинг-бот.  Демонстрация связки Telegram Mini App → локальный n8n → JS / Lua → QUIK → брокеры → биржи. Арбитраж, автоматизация и немного инженерной магии.

### n8n: Тестирование обхода Mixed Content

#### Тест 1: Простая ссылка (HTML <a>)
<a href="http://[fcac::]:5678" style="text-decoration: none;">
  <button style="cursor: pointer;">porebrik.spb.ru (Standard)</button>
</a>
*Результат: **FAIL** (Mixed Content Error)*

#### Тест 2: Ссылка с target="_blank"
<a href="http://[fcac::]:5678" target="_blank" style="text-decoration: none;">
  <button style="cursor: pointer;">porebrik.spb.ru (Target _blank)</button>
</a>
*Результат: Ожидание теста*

#### Тест 3: Ссылка через HTTPS
<a href="https://[fcac::]:5678" style="text-decoration: none;">
  <button style="cursor: pointer;">porebrik.spb.ru (HTTPS)</button>
</a>
*Результат: Ожидание теста*

#### Тест 4: JS window.open (может быть вырезано GitHub)
<button onclick="window.open('http://[fcac::]:5678', '_blank')" style="cursor: pointer;">porebrik.spb.ru (JS window.open)</button>
*Результат: Ожидание теста*
