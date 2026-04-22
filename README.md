# So2-auto-sell

Скрипт для **Perfect Click** (упрощённый синтаксис, без объектов),
в котором можно отдельно задать:
- цену продажи,
- координаты кнопок,
- **координаты поля ввода цены**.

```js
// ===== НАСТРОЙКИ =====
var PRICE = "50.00"; // цена продажи

// Координаты кнопок/элементов (подставь свои)
var sellX = 540;
var sellY = 1765;

var skinX = 540;
var skinY = 620;

// Координаты поля ВВОДА ЦЕНЫ
var priceFieldX = 540;
var priceFieldY = 1450;

var okX = 740;
var okY = 1700;

var createX = 540;
var createY = 1850;

// ===== СЦЕНАРИЙ =====
sleep(2000); // время переключиться в игру

click(sellX, sellY);
sleep(1000);

click(skinX, skinY);
sleep(1000);

// Клик по полю ввода цены
click(priceFieldX, priceFieldY);
sleep(600);

// Ввод цены (если функция поддерживается твоей версией)
if (typeof setText === "function") {
  setText(PRICE);
  sleep(500);
}

click(okX, okY);
sleep(900);

click(createX, createY);
sleep(900);
```

Если у тебя в Perfect Click не работает `setText`, оставь только клик по `priceFieldX/priceFieldY` и вводи цену вручную с клавиатуры.
