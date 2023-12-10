# Sakhteman-dade
from operator import itemgetter

def selection_sort(data):
    n = len(data)

    for i in range(n - 1):
        # پیدا کردن کمترین مقدار باقی‌مانده
        min_index = i
        for j in range(i + 1, n):
            if (data[j]['First Name'], data[j]['Last Name']) < (data[min_index]['First Name'], data[min_index]['Last Name']):
                min_index = j

        # جابجایی افراد
        data[i], data[min_index] = data[min_index], data[i]

# داده‌های اولیه
data = [
    {'First Name': 'Aahana', 'Last Name': 'Arora'},
    {'First Name': 'Armaan', 'Last Name': 'Dadra'},
    {'First Name': 'Armaan', 'Last Name': 'Kumar'},
    # ... سایر داده‌ها
    {'First Name': 'Suraj', 'Last Name': 'Sharma'}
]

# اعمال الگوریتم Selection Sort
selection_sort(data)

# نمایش داده‌های مرتب‌شده
print(data)

#الگوریتم مرتب‌سازی انتخابی (Selection Sort) اینجا به کار گرفته شده است. در این الگوریتم، در هر مرحله کمترین مقدار از باقی‌مانده انتخاب شده و با عنصر جاری جابجا می‌شود. مرتبه اجرای این الگوریتم برابر با O(n^2) است، زیرا برای هر عنصر، یک مقایسه در داخل حلقه دیگری انجام می‌شود.