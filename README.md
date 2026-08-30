# looklie-kiz-scanner

Статическая страница-сканер (Telegram WebApp) для бота
[«КИЗ Ввод и Вывод»](https://github.com/lexysav1978) сети LOOKLIE — режим
«Восстановление КИЗ». Открывается внутри Telegram по HTTPS-ссылке из
inline-кнопки с полем `web_app`, включает камеру телефона и распознаёт коды
маркировки Data Matrix (Честный знак / КИЗ) через
[zxing-wasm](https://github.com/Sec-ant/zxing-wasm).

Один файл `index.html`, без сборки. Список отсканированных кодов копится на
экране; по кнопке «Готово» страница отправляет их боту через
`Telegram.WebApp.sendData()` и закрывается — сама страница ни с каким
сервером не общается, вся логика (юрлицо, причина, очередь на подпись) — в
самом боте.

Хостится на GitHub Pages: `https://lexysav1978.github.io/looklie-kiz-scanner/`.
