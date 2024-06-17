# ttkbootstrap_Resolved
In this repository I want to publish some errors that I found in "widgets.py" file which is located at "C:\Users\vyusu\PycharmProjects\pano\venv\Lib\site-packages\ttkbootstrap" and "dialogs.py" file which is located at "C:\Users\vyusu\AppData\Local\Programs\Python\Python39\lib\site-packages\ttkbootstrap\dialogs\dialogs.py".

File "C:\Users\vyusu\AppData\Local\Programs\Python\Python39\lib\site-packages\ttkbootstrap\dialogs\dialogs.py", line 566, in DatePickerDialog
    locale.setlocale(locale.LC_ALL, locale.setlocale(locale.LC_TIME, ""))

locale.setlocale(locale.LC_ALL, locale.setlocale(locale.LC_TIME, "")) removed.

 File "C:\Users\vyusu\AppData\Local\Programs\Python\Python39\lib\site-packages\ttkbootstrap\widgets.py", line 856, in _draw_meter
    img.resize((self._metersize, self._metersize), Image.CUBIC)

"Image.CUBIC" changed with it's current state, "Image.BICUBIC"

 File "C:\Users\vyusu\AppData\Local\Programs\Python\Python39\lib\site-packages\ttkbootstrap\widgets.py", line 1065, in _configure_set
    self._metersize = utility.scale_size(kwargs.pop("metersize"))
TypeError: scale_size() missing 1 required positional argument: 'size'

utility.scale_size() removed.

File "C:\Users\vyusu\AppData\Local\Programs\Python\Python39\lib\site-packages\ttkbootstrap\widgets.py", line 1075, in _configure_set
    self._meterthickness = self.scale_size(
AttributeError: 'Meter' object has no attribute 'scale_size'

As it mentioned above, self.scale_size() should be removed.
