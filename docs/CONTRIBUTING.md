Как помочь проекту MiniArch

🎨 Хочешь сделать графический интерфейс?

Отлично! Вот несколько способов:

Вариант 1: Через tkinter (самый простой)

Создай файл `gui_demo.py` в папке `apps/`:

python
import tkinter as tk

    def run():
        window = tk.Tk()
        window.title("MiniArch GUI")
        window.geometry("400x300")
    
    label = tk.Label(window, text="Добро пожаловать в MiniArch!", 
                    font=("Arial", 14))
    label.pack(pady=20)
    
    button = tk.Button(window, text="Нажми меня", 
                      command=lambda: print("Кнопка нажата!"))
    button.pack()
    
    window.mainloop()

if __name__ == "__main__":
    run()

Вариант 2: Через pygame (для игр)
import pygame

    def run():
        pygame.init()
        screen = pygame.display.set_mode((800, 600))
        pygame.display.set_caption("MiniArch Game")
    
    running = True
    while running:
        for event in pygame.event.get():
            if event.type == pygame.QUIT:
                running = False
        
        screen.fill((0, 0, 0))
        pygame.display.flip()
    
    pygame.quit()

    
Как создать свой модуль для системы
Создай файл в папке modules/ или apps/

Обязательно добавь функцию run()

Можешь использовать объект system для доступа к функциям ОС

Пример модуля hello.py:

    def run(system):
        """Приветственный модуль"""
        system.clear_screen()
        print(system.colorize("👋 Привет из модуля!", "green"))
        name = input("Как тебя зовут? ")
        print(f"Приятно познакомиться, {name}!")
        input("\nНажми Enter...")

🎯 Правила оформления кода

Используй 4 пробела для отступов

Комментируй сложные места

Добавляй описание к каждой новой команде

Тестируй перед отправкой
