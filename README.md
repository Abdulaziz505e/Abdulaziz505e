import tkinter as tk
from time import strftime

def update_time():
    current_time = strftime('%H:%M:%S %p')
    label.config(text=current_time)
    label.after(1000, update_time)  # تحديث كل ثانية

# إنشاء نافذة التطبيق
root = tk.Tk()
root.title("ساعة رقمية")

# إعداد النص والتصميم
label = tk.Label(root, font=('Arial', 50), background='black', foreground='cyan')
label.pack(anchor='center')

# تشغيل تحديث الوقت
update_time()

# تشغيل التطبيق
root.mainloop()
