# PyLadies Shop
This e-commerce was created using [Shuup Open Source E-commerce](https://github.com/shuup/shuup).

## Development Instructions

1. Clone the repository
2. Create virtualenv
3. Activate virtualenv
4. Install dependencies
5. Execute python migrations
6. Text missing (shuup_init)
7. Run local server, access http://localhost:8000/admin/ in a browser and check that a "Maintenance message" is prompted 
8. Install `ipdb` (just for debugging)
9. Start project shell and set `maintenance_mode` to `false`
10. Install front-end resources
11. Create a superuser for Admin

```console
git clone https://github.com/pyladies-brazil/lojinha.git
python -m venv .env
source .env/bin/activate
pip install -e .
python -m shuup_workbench migrate
python -m shuup_workbench shuup_init
python -m shuup_workbench runserver
pip install ipdb
python -m shuup_workbench shell
    from shuup.core.models import Shop
    shop = Shop.objects.get()
    shop.maintenance_mode = False
    shop.save()
python setup.py build_resources
python -m shuup_workbench createsuperuser
```