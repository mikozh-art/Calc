# PWA Калькулятор

Ці файли додають підтримку Progressive Web App (PWA) для твого калькулятора.

## Файли:
- manifest.json — опис програми та іконки
- sw.js — service worker для кешування
- icons/icon-192.png, icons/icon-512.png — іконки додатку

## Як встановити:
1. Скопіюй ці файли у корінь твого GitHub репозиторію калькулятора.
2. Додай у index.html:
   У <head>:
   <link rel="manifest" href="manifest.json">
   <meta name="theme-color" content="#4CAF50">

   Перед </body>:
   <script>
   if ('serviceWorker' in navigator) {
     navigator.serviceWorker.register('./sw.js');
   }
   </script>
3. Закоміть та запуш зміни в main гілку.
4. Зайди на сайт з телефону та додай на головний екран.
