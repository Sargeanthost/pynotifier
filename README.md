## Desktop Notifications

Simple cross-platform (Windows/Linux) Python3 module for displaying desktop notifications. This fork, in combination with the other fork of *win10toast* on my profile, allows clickable Windows 10 notifications.

### Installation
```bash
$ pip install py-notifier
```
Replace files with this repository

### Requirements
If running on Windows: `win10toast`

### Example
```python
from pynotifier import Notification
import webbrowser

Notification(
	title='Notification Title',
	description='Notification Description',
	icon_path='path/to/image/file/icon.png', # On Windows .ico is required, on Linux - .png
	duration=5,                              # Duration in seconds
	urgency=Notification.URGENCY_CRITICAL,
	callback_on_click = lambda: webbrowser.open(message, new=0, autoraise=True)
).send()
```

### Author
* [Yuriy Lisovskiy](https://github.com/YuriyLisovskiy)

### License
The project is licensed under the terms of the [GNU General Public License v3.0](https://opensource.org/licenses/GPL-3.0), see the [LICENSE](LICENSE) file for more information.
