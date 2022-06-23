# PyInv 

Online Quartermaster and Inventory System.

### Features

- Based around a hierarchical tree of nodes, some of which are assets.
- Assets are uniquely identified by one or more asset codes.
- Track asset models and manufacturers
- Multiple Asset Code Formats:
    - UUID
    - Arbitrary String
    - Human-friendly Asset Code format with Damm checksum
- REST API
- Django Admin for back office access to data

### Planned

- Track countable items, where only the quantity and location matter
- Powerful auditing engine
- Printer Support
- Report generation
- Barcode scanner support

## Deployment

PyInv requires Python 3.8 or higher.

The [Django deployment guidelines](https://docs.djangoproject.com/en/3.2/howto/deployment/) are and should be used.

You need to copy `configuration.example.py` to `pyinv/pyinv/configuration.py` and configure your database and email settings.

You'll need to run a couple of management commands to get going:

```bash
./manage.py migrate
./manage.py createsuperuser
```