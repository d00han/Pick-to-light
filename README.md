# Put to Light System: Comprehensive Development Overview
[![en](https://img.shields.io/badge/lang-en-red.svg)](/README.md)
[![ru](https://img.shields.io/badge/lang-ru-green.svg)](/README.ru.md)
## About the Project

This project is an implementation of a "Put to Light" system designed to optimize the sorting process in a warehouse. The main goal of the system is to guide operators to the correct bins and indicate the quantity of items to place. The system was entirely designed, developed, and integrated by me.

---

## System Functionality

1. The worker scans the product barcode using a scanner.
2. The screens installed on the bins display the required quantity of items to place.
3. After placing the items, the operator confirms the task by pressing a button.

---

## My Role in the Project

### 1. Requirements Analysis:
- Studied the client’s needs and warehouse conditions.
- Defined the system’s functionality and architecture.

### 2. Component Selection:
- Chose STM32F103C8T6 microcontrollers for their optimal performance-to-cost ratio.
- Used seven-segment displays for clear information presentation.
- Applied TJA1050 CAN transceivers for reliable data exchange between modules.

### 3. PCB Design and Module Assembly:
- Designed and ordered PCBs.
- Assembled components on the boards and tested the finished devices.

<p align="center">
  <img src="/assets/render_top.png" alt="PCB rendering top" width="45%">
  <img src="/assets/render_bottom.png" alt="PCB rendering bottom" width="45%">
</p>


### 4. Microcontroller Programming:
- Developed firmware for STM32 microcontrollers using the CAN protocol.
- Implemented button input handling and seven-segment display management.

### 5. Server-Side Service Creation:
- Built a service in C# for the mini-PC, performing the following functions:
  - Communicating with the client’s server to receive tasks.
  - Managing system logic and task distribution among modules.
  - Confirming task completion on the server.

### 6. Integration and Testing:
- Integrated the system at the client’s warehouse.
- Tested functionality under real conditions.
- Made refinements to enhance efficiency and usability.

---

## Technical Aspects

### Network Interaction:
- Utilized the CAN protocol for data exchange between modules, ensuring reliable communication even in high electromagnetic interference environments.

### Hardware:
- The main module connects to a mini-PC, serving as a link between the system and the server.
- Each bin is equipped with a separate module containing a microcontroller, display, and buttons.

### Software:
- Firmware for microcontrollers was written in C, focusing on reliability and performance.
- The server-side service in C# uses REST API for communication with the client’s server.

---

## Results

The system implementation resulted in:
- Increased speed and accuracy of item sorting.
- Reduced operator errors.
- Improved transparency and control over task execution in the warehouse.

---

## Conclusion

This project highlights my comprehensive approach to development: from requirements analysis and component selection to programming and system integration at the warehouse. The system operates successfully and fully meets the client’s demands, proving its reliability and effectiveness.

---

# Система Put to Light: Комплексный обзор разработки

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
