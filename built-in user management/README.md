<h1>Django Built-In User Management</h1>

```
python manage.py migrate
```

<h4>Super User</h4>

```
python manage.py createsuperuser
```

<h4>User Authentication</h4>
<h5>Import</h5>

```python
from django.contrib.auth.decorators import login_required
```

```python
@login_required(login_url='/admin')
def auth(request):
```
