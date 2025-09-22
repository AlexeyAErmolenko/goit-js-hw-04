# goit-js-hw-04 <br> 
    розуміти, що таке об'єкт у JavaScript і як його створити; <br>
    навчитися додавати та змінювати значення властивостей об'єкта; <br>
    дізнатися про доступні способи перебирання об’єкту; <br>
    вміти працювати з масивом однотипних об'єктів; <br>
    навчитися звертатися до властивості об'єкта в його методах (блок 4); <br>
    використовувати сучасний синтаксис spread і rest та розуміти його функціонал. <br>
     <br>
Задача 1. Пакування товарів <br>
Виконуй це завдання у файлі task-1.js <br>
Напиши функцію isEnoughCapacity(products, containerSize), яка обчислює, чи помістяться всі товари в контейнер при пакуванні. <br>
Функція оголошує два параметри: <br>
    products — об’єкт, у якому ключі містять назви товарів, а їхні значення — кількість цих товарів. Наприклад, { apples: 2, grapes: 4 }. <br>
    containerSize — число, максимальна кількість одиниць товарів, яку в себе може вмістити контейнер. <br>
Функція має повернути результат перевірки, чи помістяться всі товари в контейнер. Тобто порахувати загальну кількість товарів в об’єкті products і повернути true, якщо вона менше або дорівнює containerSize, і false, якщо ні. <br>
Візьми код нижче і встав після оголошення своєї функції для перевірки коректності її роботи. У консоль будуть виведені результати її викликів. <br>
console.log( <br>
  isEnoughCapacity({ apples: 2, grapes: 3, carrots: 1 }, 8) <br>
); // true <br>
console.log( <br>
  isEnoughCapacity({ apples: 4, grapes: 6, lime: 16 }, 12) <br>
); // false <br>
console.log( <br>
  isEnoughCapacity({ apples: 1, lime: 5, tomatoes: 3 }, 14) <br>
); // true <br>
console.log( <br>
  isEnoughCapacity({ apples: 18, potatoes: 5, oranges: 2 }, 7) <br>
); // false <br>
 <br>
Задача 2. Розрахунок калорій <br>
Виконуй це завдання у файлі task-2.js <br>
Напиши функцію calcAverageCalories(days), яка повертає середньодобове значення кількості калорій, які спортсмен споживав протягом тижня. Функція очікує один параметр: days — масив об’єктів. Кожен об’єкт описує день тижня та кількість калорій calories, спожитих спортсменом, у цей день. Візьми код нижче і встав після оголошення своєї функції для перевірки коректності її роботи. У консоль будуть виведені результати її викликів. <br>
console.log( <br>
  calcAverageCalories([ <br>
    { day: "monday", calories: 3010 }, <br>
    { day: "tuesday", calories: 3200 }, <br>
    { day: "wednesday", calories: 3120 }, <br>
    { day: "thursday", calories: 2900 }, <br>
    { day: "friday", calories: 3450 }, <br>
    { day: "saturday", calories: 3280 }, <br>
    { day: "sunday", calories: 3300 } <br>
  ]) <br>
); // 3180 <br>
 <br>
console.log( <br>
  calcAverageCalories([ <br>
    { day: "monday", calories: 2040 }, <br>
    { day: "tuesday", calories: 2270 }, <br>
    { day: "wednesday", calories: 2420 }, <br>
    { day: "thursday", calories: 1900 }, <br>
    { day: "friday", calories: 2370 }, <br>
    { day: "saturday", calories: 2280 }, <br>
    { day: "sunday", calories: 2610 } <br>
  ]) <br>
); // 2270 <br>
 <br>
console.log( <br>
  calcAverageCalories([]) <br>
); // 0 <br>
 <br>
Залиш цей код для перевірки ментором. <br>
На що буде звертати увагу ментор при перевірці: <br>
Оголошена функція calcAverageCalories(days) <br>
Такий виклик функції calcAverageCalories повертає 3180 <br>
 <br>
calcAverageCalories([ <br>
  { day: "monday", calories: 3010 }, <br>
  { day: "tuesday", calories: 3200 }, <br>
  { day: "wednesday", calories: 3120 }, <br>
  { day: "thursday", calories: 2900 }, <br>
  { day: "friday", calories: 3450 }, <br>
  { day: "saturday", calories: 3280 }, <br>
  { day: "sunday", calories: 3300 } <br>
]) <br>
Такий виклик функції calcAverageCalories повертає 2270 <br>
 <br>
calcAverageCalories([ <br>
  { day: "monday", calories: 2040 }, <br>
  { day: "tuesday", calories: 2270 }, <br>
  { day: "wednesday", calories: 2420 }, <br>
  { day: "thursday", calories: 1900 }, <br>
  { day: "friday", calories: 2370 }, <br>
  { day: "saturday", calories: 2280 }, <br>
  { day: "sunday", calories: 2610 } <br>
]) <br>
Такий виклик функції calcAverageCalories повертає 0 <br>
 <br>
calcAverageCalories([]) <br>
 <br>
Задача 3. Профіль гравця <br>
Виконуй це завдання у файлі task-3.js <br>
Об’єкт profile описує профіль користувача на ігровій платформі. У його властивостях зберігається ім’я профілю username та кількість активних годин playTime, проведених у грі. <br>
const profile = { <br>
    username: "Jacob", <br>
  playTime: 300, <br>
}; <br>
 <br>
Доповни об’єкт profile методами для роботи з його властивостями. <br>
    Метод changeUsername(newName) повинен приймати рядок (нове ім’я) в параметр newName та змінювати значення властивості username на нове. Нічого не повертає. <br>
    Метод updatePlayTime(hours) повинен приймати число (кількість годин) у параметр hours та збільшити на нього значення властивості playTime. Нічого не повертає. <br>
    Метод getInfo() має повертати рядок формату <Username> has <amount> active hours!, де <Username> — це ім’я профілю, а <amount> — кількість ігрових годин. <br>
Візьми код нижче і встав після оголошення своєї функції для перевірки коректності її роботи. У консоль будуть виведені результати її роботи. <br>
console.log(profile.getInfo()); // "Jacob has 300 active hours!" <br>
profile.changeUsername("Marco"); <br>
console.log(profile.getInfo()); // "Marco has 300 active hours!" <br>
profile.updatePlayTime(20); <br>
console.log(profile.getInfo()); // "Marco has 320 active hours!" <br>
Залиш цей код для перевірки ментором. <br>
На що буде звертати увагу ментор при перевірці: <br>
    Оголошена змінна profile <br>
    Значення змінної profile — це об’єкт з властивостями username, playTime, getInfo, changeUsername і updatePlayTime <br>
    Значення властивості getInfo — це функція <br>
    Значення властивості changeUsername — це функція <br>
    Значення властивості updatePlayTime — це функція <br>
    Для звернення до властивостей об’єкта в його методах використовується this
