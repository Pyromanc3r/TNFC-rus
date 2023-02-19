# TNFC-rus
### **Комплект файлов для перевода модпака TechNodeFirmaCraft 3.7.1 для Minecraft версии 1.7.10**

Желание перевести модпак появилось спонтанно. В оригинальной версии многие квесты имели скудное описание, а местами и вовсе отсутствовало таковое. Также, некоторые квесты были забагованы и не завершались. Я добавил расширенное описание квестов и механик где посчитал, что это необходимо. Объем текста вырос примерно на треть от оригинала. Хоть мод Hardcore Quest Mode (HQM) и не очень подходит под большие страницы текста, но я постарался более-менее структурировать информацию.

Форматирование теста мод не поддерживает вообще, а только спам пробелов. Не знаю, вылезут ли косяки с отступами и разрывами строк на высоких разрешениях экрана. Подгонялось всё под стандартное 1920x1080 с интерфейсом в игре "Крупный" и модом ClientFixer (фиксит масштабирование интерфейса игры для рус. локализации).
За грамматику пардоньте, как говорится, но я не гуру и не лингвист. В оригинальном тексте частенько проскакивали отсылки, мемасы и игра слов. Адаптировал как сумел.
Буква "ё" заменена в тексте на "е". Из-за неё (возможно) были периодические рандомные краши клиента при тесте. Очень странное поведение. Я не стал рисковать и заменил её. 

---

## Установка:
1. Сам модпак лежит на оф. сайте лаунчера - ATLauncher https://atlauncher.com/pack/technodefirmacraft. Выделенный сервер доступен только через их лаунчер. Также модпак можно скачать и через MultiMC лаунчер. Вам нужен лиц. аккаунт для этого.
2. Замените файл **quests.hqm** в папке ...\config\hqm. Это русификация книги квестов.
3. Удалите папку **igwmod** в корневой папке модпака и замените её скаченной. Это внутриигровая "мини Википедия" с дополнительной информацией о модах. В игре вызывается на клавишу **"I"**. Переведён раздел только о TFC (TerraFirmaCraft).

Также, в игре можно импортировать .json файлы квестов в квестбук. На случай, если захотите что-то исправить. Но этот процесс специфический и не очень надежный. Можно поломать цепочки и главы квестов. А также, им невозможно изменить титульное приветствие (оно хранится в главном файле "quests.hqm").

Для этого откройте файл конфигурации **editmode.cfg** в ...\config\hqm и измените параметр

B:UseEditor=false на true. Это активирует режим редактирования квестбука. Затем удалите файл **quests.hqm**.
Также создайте папку **QuestFiles** в той же директории ...\config\hqm, если её нет. Поместите туда файл **"reputations.json"** и только один файл главы. Например, **"Каменная эра.json"**.

В игре создайте мир с разрешёнными читами и активируйте систему квестов командой:

**/hqm quest**

Импортируйте квест первой главы командой:

**/hqm load all**

Удалите файл **"Каменная эра.json"** из папки **QuestFiles** и положите на его место следующую главу, а файл **"reputations.json"** не трогайте.

И так со всеми главами последовательно.

Если положить разом все файлы и импортировать, то главы перемешаются и цепочки заданий поломаются.

---

### **Прочие команды квестбука** (читы в игре должны быть включены):

**/hqm quest**
- активирует систему квестов вручную. На случай, если квестбук не выдался при старте игры (а такое иногда бывает).

**/hqm edit**
- выдает специальную квестовую книгу для операторов. В ней можно мгновенно завершать и откатывать квесты при нажатии Shift+ЛКМ по иконке квеста. На случай, если забагуется какой-нибудь квест. Файл конфигурации **editmode.cfg** должен быть изменён как написано выше.

**/hqm save all**
- сохраняет .json файлы глав квестов в папку **QuestFiles**.

**/hqm load all**
- загружает их от туда.

**/hqm help**
- показывает доступные команды.

**/hqm enable**
- активирует режим хардкора. Игрокам выдаётся 20 жизней. Если их растратить, то на на карту больше не зайти. Game Over.

**/hqm hardcore disable**
- отключает режим хардкора. Квесты делать всё ещё можно.
