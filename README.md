1. Как организованны данные в компьютере? Типы данных
1 - Текстовые данные 2 - Двоичные данные(последовательность байтов)

2. Как сбросить и восстановить систему?
Параметры windows
Обновление и безопасность
Восстановление
Начать под вернуть ПК в исходное состояние

Задача: 
import random
from datetime import datetime, timedelta
class Date:

    today = datetime.now()
    manufacture_date = today - timedelta(days = random.randint(0,6))
    
    price = random.randint(50,200)
    expire_days = random.randint(1,7)
    
    print(f"Дата изготовления:{manufacture_date.strftime('%d.%m.%Y')}")
    print(f"Цена:{price} рублей")
    print(f"Срок:{expire_days} дней")

    if manufacture_date == today:
        final_price = price;
    elif today > manufacture_date + timedelta(days=expire_days):
        final_price = 0;
    else:
        final_price = price;
        
    print(f"Цена:{final_price} рублей")
