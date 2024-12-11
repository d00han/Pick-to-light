# Система Put to Light: Комплексный обзор разработки
[![en](https://img.shields.io/badge/lang-en-red.svg)](/README.md)
[![ru](https://img.shields.io/badge/lang-ru-green.svg)](/README.ru.md)
## О проекте

Данный проект представляет собой реализацию системы "Put to Light", которая предназначена для оптимизации процесса сортировки товаров на складе. Основная задача системы — направить оператора к правильным ячейкам и указать необходимое количество товара для размещения. Система была полностью спроектирована, разработана и интегрирована мной.

---

## Функционал системы

1. Работник сканирует штрих-код товара с помощью сканера.
2. На экранах, установленных на ячейках, загорается требуемое количество товара для размещения.
3. После размещения товара оператор подтверждает выполнение задачи нажатием кнопки.

---

## Моя роль в проекте

### 1. Анализ требований:
- Изучение потребностей клиента и условий склада.
- Определение функциональности системы и её архитектуры.

### 2. Подбор компонентов:
- Выбор микроконтроллеров STM32F103C8T6 за их оптимальное соотношение производительности и стоимости.
- Использование семисегментных индикаторов для наглядного отображения информации.
- Применение CAN-трансиверов TJA1050 для надёжного обмена данными между модулями.

### 3. Разработка печатных плат и сборка модулей:
- Проектирование и заказ печатных плат.
- Монтаж компонентов на платы и тестирование готовых устройств.

<p align="center">
  <img src="/assets/render_top.png" alt="PCB rendering top" width="45%">
  <img src="/assets/render_bottom.png" alt="PCB rendering bottom" width="45%">
</p>

### 4. Программирование микроконтроллеров:
- Разработка прошивки для микроконтроллеров STM32 с использованием протокола CAN.
- Реализация обработки ввода с кнопок и управления семисегментными индикаторами.

### 5. Создание серверной службы:
- Разработка службы на C# для мини-ПК, которая выполняет следующие функции:
  - Общение с сервером клиента для получения задач.
  - Управление логикой работы системы и распределением задач между модулями.
  - Подтверждение выполнения задач на сервере.

### 6. Интеграция и тестирование:
- Интеграция системы на складе заказчика.
- Тестирование функциональности в реальных условиях.
- Внесение доработок для повышения эффективности и удобства эксплуатации.

---

## Технические аспекты

### Сетевое взаимодействие:
- Использован протокол CAN для обмена данными между модулями. Это обеспечило надёжность передачи данных даже в условиях высоких электромагнитных помех.

### Аппаратная часть:
- Главный модуль системы подключён к мини-ПК, который служит связующим звеном между системой и сервером.
- Каждая ячейка оснащена отдельным модулем с микроконтроллером, индикатором и кнопками.

### Программное обеспечение:
- Прошивка микроконтроллеров написана на C с акцентом на надёжность и быстродействие.
- Серверная служба на C# использует REST API для взаимодействия с сервером заказчика.

---

## Результаты

В результате внедрения системы:
- Увеличилась скорость и точность сортировки товаров.
- Уменьшилось количество ошибок со стороны операторов.
- Улучшилась прозрачность и контроль выполнения задач на складе.

---

## Вывод

Этот проект демонстрирует мой всесторонний подход к разработке: от анализа требований и подбора компонентов до программирования и интеграции системы на складе. Система успешно функционирует и полностью удовлетворяет запросы заказчика, что подтверждает её надёжность и эффективность.