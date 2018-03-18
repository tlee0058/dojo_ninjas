C:\Users\TL\Documents\python_stack\django\users>python manage.py startapp dojo_ninjas

C:\Users\TL\Documents\python_stack\django\users>python manage.py runserver
Performing system checks...

Unhandled exception in thread started by <function wrapper at 0x0000000006CD3CF8>
Traceback (most recent call last):
  File "C:\Python27\lib\site-packages\django\utils\autoreload.py", line 228, in wrapper
    fn(*args, **kwargs)
  File "C:\Python27\lib\site-packages\django\core\management\commands\runserver.py", line 124, in inner_run
    self.check(display_num_errors=True)
  File "C:\Python27\lib\site-packages\django\core\management\base.py", line 359, in check
    include_deployment_checks=include_deployment_checks,
  File "C:\Python27\lib\site-packages\django\core\management\base.py", line 346, in _run_checks
    return checks.run_checks(**kwargs)
  File "C:\Python27\lib\site-packages\django\core\checks\registry.py", line 81, in run_checks
    new_errors = check(app_configs=app_configs)
  File "C:\Python27\lib\site-packages\django\core\checks\urls.py", line 16, in check_url_config
    return check_resolver(resolver)
  File "C:\Python27\lib\site-packages\django\core\checks\urls.py", line 26, in check_resolver
    return check_method()
  File "C:\Python27\lib\site-packages\django\urls\resolvers.py", line 254, in check
    for pattern in self.url_patterns:
  File "C:\Python27\lib\site-packages\django\utils\functional.py", line 35, in __get__
    res = instance.__dict__[self.name] = self.func(instance)
  File "C:\Python27\lib\site-packages\django\urls\resolvers.py", line 405, in url_patterns
    patterns = getattr(self.urlconf_module, "urlpatterns", self.urlconf_module)
  File "C:\Python27\lib\site-packages\django\utils\functional.py", line 35, in __get__
    res = instance.__dict__[self.name] = self.func(instance)
  File "C:\Python27\lib\site-packages\django\urls\resolvers.py", line 398, in urlconf_module
    return import_module(self.urlconf_name)
  File "C:\Python27\lib\importlib\__init__.py", line 37, in import_module
    __import__(name)
  File "C:\Users\TL\Documents\python_stack\django\users\users\urls.py", line 22, in <module>
    url(r'^', include("apps.dojo_ninjas_urls")),
  File "C:\Python27\lib\site-packages\django\conf\urls\__init__.py", line 50, in include
    urlconf_module = import_module(urlconf_module)
  File "C:\Python27\lib\importlib\__init__.py", line 37, in import_module
    __import__(name)
ImportError: No module named dojo_ninjas_urls

C:\Users\TL\Documents\python_stack\django\users>python manage.py runserver
Performing system checks...

System check identified no issues (0 silenced).
March 17, 2018 - 16:32:16
Django version 1.11.11, using settings 'users.settings'
Starting development server at http://127.0.0.1:8000/
Quit the server with CTRL-BREAK.
[17/Mar/2018 16:32:23] "GET / HTTP/1.1" 200 5
[17/Mar/2018 16:32:28] "GET / HTTP/1.1" 200 5

C:\Users\TL\Documents\python_stack\django\users>python manage.py makemigrations
Migrations for 'dojo_ninjas':
  apps\dojo_ninjas\migrations\0001_initial.py
    - Create model Dojo
    - Create model Ninja

C:\Users\TL\Documents\python_stack\django\users>python manage.py migrate
Operations to perform:
  Apply all migrations: admin, auth, contenttypes, dojo_ninjas, sessions, user_login
Running migrations:
  Applying dojo_ninjas.0001_initial... OK

C:\Users\TL\Documents\python_stack\django\users>python manage.py shell
Python 2.7.13 (v2.7.13:a06454b1afa1, Dec 17 2016, 20:53:40) [MSC v.1500 64 bit (AMD64)]
Type "copyright", "credits" or "license" for more information.

IPython 5.5.0 -- An enhanced Interactive Python.
?         -> Introduction and overview of IPython's features.
%quickref -> Quick reference.
help      -> Python's own help system.
object?   -> Details about 'object', use 'object??' for extra details.

In [1]: Dojo.objects.create(name="CodingDojo Silicon Valley", city="Mountain View", state="CA")
---------------------------------------------------------------------------
NameError                                 Traceback (most recent call last)
<ipython-input-1-9cc3a2d9ddba> in <module>()
----> 1 Dojo.objects.create(name="CodingDojo Silicon Valley", city="Mountain View", state="CA")

NameError: name 'Dojo' is not defined

In [2]: dojo1 = Dojo.objects.create(name="CodingDojo Silicon Valley", city="Mountain View", state="CA")
---------------------------------------------------------------------------
NameError                                 Traceback (most recent call last)
<ipython-input-2-f61b1f2bde91> in <module>()
----> 1 dojo1 = Dojo.objects.create(name="CodingDojo Silicon Valley", city="Mountain View", state="CA")

NameError: name 'Dojo' is not defined

In [3]: exit()

C:\Users\TL\Documents\python_stack\django\users>cd apps\dojo_ninjas

C:\Users\TL\Documents\python_stack\django\users\apps\dojo_ninjas>python ...\manage.py shell
python: can't open file '...\manage.py': [Errno 2] No such file or directory

C:\Users\TL\Documents\python_stack\django\users\apps\dojo_ninjas>python ....\manage.py shell
python: can't open file '....\manage.py': [Errno 2] No such file or directory

C:\Users\TL\Documents\python_stack\django\users\apps\dojo_ninjas>cd ..

C:\Users\TL\Documents\python_stack\django\users\apps>cd ..

C:\Users\TL\Documents\python_stack\django\users>python manage.py shell
Python 2.7.13 (v2.7.13:a06454b1afa1, Dec 17 2016, 20:53:40) [MSC v.1500 64 bit (AMD64)]
Type "copyright", "credits" or "license" for more information.

IPython 5.5.0 -- An enhanced Interactive Python.
?         -> Introduction and overview of IPython's features.
%quickref -> Quick reference.
help      -> Python's own help system.
object?   -> Details about 'object', use 'object??' for extra details.

In [1]: dojo1 = Dojo.objects.create(name="Coding Dojo Sillicon Valley", city="Mountain View", state="CA")
---------------------------------------------------------------------------
NameError                                 Traceback (most recent call last)
<ipython-input-1-3e2171a7c26b> in <module>()
----> 1 dojo1 = Dojo.objects.create(name="Coding Dojo Sillicon Valley", city="Mountain View", state="CA")

NameError: name 'Dojo' is not defined

In [2]: from apps.dojo_ninjas.models import *

In [3]: dojo1 = Dojo.objects.create(name="Coding Dojo Sillicon Valley", city="Mountain View", state="CA")

In [4]: dojo2 = Dojo.object.create(name="Coding Dojo Seattle", city = "Seattle", state="WA")
---------------------------------------------------------------------------
AttributeError                            Traceback (most recent call last)
<ipython-input-4-066391cbe0c6> in <module>()
----> 1 dojo2 = Dojo.object.create(name="Coding Dojo Seattle", city = "Seattle", state="WA")

AttributeError: type object 'Dojo' has no attribute 'object'

In [5]: dojo2 = Dojo.objects.create(name="Coding Dojo Seattle", city = "Seattle", state="WA")

In [6]: dojo3 = Dojo.objects.create(name="Coding Dojo New York", city = "New York", state="NY")

In [7]: Dojo.objects.first().ninjas.all()
Out[7]: <QuerySet []>

In [8]: ninja1 = Ninja.objects.create(first_name="Ting", last_name="Lee")
---------------------------------------------------------------------------
IntegrityError                            Traceback (most recent call last)
<ipython-input-8-7310d010e020> in <module>()
----> 1 ninja1 = Ninja.objects.create(first_name="Ting", last_name="Lee")

C:\Python27\lib\site-packages\django\db\models\manager.pyc in manager_method(self, *args, **kwargs)
     83         def create_method(name, method):
     84             def manager_method(self, *args, **kwargs):
---> 85                 return getattr(self.get_queryset(), name)(*args, **kwargs)
     86             manager_method.__name__ = method.__name__
     87             manager_method.__doc__ = method.__doc__

C:\Python27\lib\site-packages\django\db\models\query.pyc in create(self, **kwargs)
    392         obj = self.model(**kwargs)
    393         self._for_write = True
--> 394         obj.save(force_insert=True, using=self.db)
    395         return obj
    396

C:\Python27\lib\site-packages\django\db\models\base.pyc in save(self, force_insert, force_update, using, update_fields)
    806
    807         self.save_base(using=using, force_insert=force_insert,
--> 808                        force_update=force_update, update_fields=update_fields)
    809     save.alters_data = True
    810

C:\Python27\lib\site-packages\django\db\models\base.pyc in save_base(self, raw, force_insert, force_update, using, update_fields)
    836             if not raw:
    837                 self._save_parents(cls, using, update_fields)
--> 838             updated = self._save_table(raw, cls, force_insert, force_update, using, update_fields)
    839         # Store the database on which the object was saved
    840         self._state.db = using

C:\Python27\lib\site-packages\django\db\models\base.pyc in _save_table(self, raw, cls, force_insert, force_update, using, update_fields)
    922
    923             update_pk = meta.auto_field and not pk_set
--> 924             result = self._do_insert(cls._base_manager, using, fields, update_pk, raw)
    925             if update_pk:
    926                 setattr(self, meta.pk.attname, result)

C:\Python27\lib\site-packages\django\db\models\base.pyc in _do_insert(self, manager, using, fields, update_pk, raw)
    961         """
    962         return manager._insert([self], fields=fields, return_id=update_pk,
--> 963                                using=using, raw=raw)
    964
    965     def delete(self, using=None, keep_parents=False):

C:\Python27\lib\site-packages\django\db\models\manager.pyc in manager_method(self, *args, **kwargs)
     83         def create_method(name, method):
     84             def manager_method(self, *args, **kwargs):
---> 85                 return getattr(self.get_queryset(), name)(*args, **kwargs)
     86             manager_method.__name__ = method.__name__
     87             manager_method.__doc__ = method.__doc__

C:\Python27\lib\site-packages\django\db\models\query.pyc in _insert(self, objs, fields, return_id, raw, using)
   1074         query = sql.InsertQuery(self.model)
   1075         query.insert_values(fields, objs, raw=raw)
-> 1076         return query.get_compiler(using=using).execute_sql(return_id)
   1077     _insert.alters_data = True
   1078     _insert.queryset_only = False

C:\Python27\lib\site-packages\django\db\models\sql\compiler.pyc in execute_sql(self, return_id)
   1110         with self.connection.cursor() as cursor:
   1111             for sql, params in self.as_sql():
-> 1112                 cursor.execute(sql, params)
   1113             if not (return_id and cursor):
   1114                 return

C:\Python27\lib\site-packages\django\db\backends\utils.pyc in execute(self, sql, params)
     77         start = time()
     78         try:
---> 79             return super(CursorDebugWrapper, self).execute(sql, params)
     80         finally:
     81             stop = time()

C:\Python27\lib\site-packages\django\db\backends\utils.pyc in execute(self, sql, params)
     62                 return self.cursor.execute(sql)
     63             else:
---> 64                 return self.cursor.execute(sql, params)
     65
     66     def executemany(self, sql, param_list):

C:\Python27\lib\site-packages\django\db\utils.pyc in __exit__(self, exc_type, exc_value, traceback)
     92                 if dj_exc_type not in (DataError, IntegrityError):
     93                     self.wrapper.errors_occurred = True
---> 94                 six.reraise(dj_exc_type, dj_exc_value, traceback)
     95
     96     def __call__(self, func):

C:\Python27\lib\site-packages\django\db\backends\utils.pyc in execute(self, sql, params)
     62                 return self.cursor.execute(sql)
     63             else:
---> 64                 return self.cursor.execute(sql, params)
     65
     66     def executemany(self, sql, param_list):

C:\Python27\lib\site-packages\django\db\backends\sqlite3\base.pyc in execute(self, query, params)
    326             return Database.Cursor.execute(self, query)
    327         query = self.convert_query(query)
--> 328         return Database.Cursor.execute(self, query, params)
    329
    330     def executemany(self, query, param_list):

IntegrityError: NOT NULL constraint failed: dojo_ninjas_ninja.dojo_id

In [9]: this_dojo = Dojo.objects.get(id=1)

In [10]: ninja1 = Ninja.objects.create(first_name="Ting", last_name="Lee", dojo=this_dojo)

In [11]: ninja2 = Ninja.objects.create(first_name="Nga", last_name="Lee", dojo=this_dojo)

In [12]: Dojo.objects.first().ninjas.all()
Out[12]: <QuerySet [<Ninja: Ninja object>, <Ninja: Ninja object>]>

In [13]: Ninja.objects.first().dojo
Out[13]: <Dojo: Dojo object>

In [14]: b = Dojo.objects.get(id=1)

In [15]: b.delete()
Out[15]: (3, {u'dojo_ninjas.Dojo': 1, u'dojo_ninjas.Ninja': 2})

In [16]: a = Dojo.objects.get(id=2)

In [17]: a.delete()
Out[17]: (1, {u'dojo_ninjas.Dojo': 1, u'dojo_ninjas.Ninja': 0})

In [18]: c = Dojo.objects.get(id=3)

In [19]: c.delete()
Out[19]: (1, {u'dojo_ninjas.Dojo': 1, u'dojo_ninjas.Ninja': 0})

In [20]: dojo1 = Dojo.objects.create(name="Coding Dojo SV", city="Mountain View", state="CA")

In [21]: dojo2 = Dojo.objects.create(name="Coding Dojo DC", city="Washington DC", state="DC")

In [22]: dojo3 = Dojo.objects.create(name="Coding Dojo NY", city="New York", state="NY")

In [23]: first_dojo = Dojo.objects.get(id=1)
---------------------------------------------------------------------------
DoesNotExist                              Traceback (most recent call last)
<ipython-input-23-0736016a7b0a> in <module>()
----> 1 first_dojo = Dojo.objects.get(id=1)

C:\Python27\lib\site-packages\django\db\models\manager.pyc in manager_method(self, *args, **kwargs)
     83         def create_method(name, method):
     84             def manager_method(self, *args, **kwargs):
---> 85                 return getattr(self.get_queryset(), name)(*args, **kwargs)
     86             manager_method.__name__ = method.__name__
     87             manager_method.__doc__ = method.__doc__

C:\Python27\lib\site-packages\django\db\models\query.pyc in get(self, *args, **kwargs)
    378             raise self.model.DoesNotExist(
    379                 "%s matching query does not exist." %
--> 380                 self.model._meta.object_name
    381             )
    382         raise self.model.MultipleObjectsReturned(

DoesNotExist: Dojo matching query does not exist.

In [24]: first_dojo = Dojo.objects.get(id=4)

In [25]: ninja1 = Ninja.objects.create(first_name="Ting", last_name="Lee", dojo=first_dojo)

In [26]: ninja2 = Ninja.objects.create(first_name="Nga", last_name="Lee", dojo=first_dojo)

In [27]: ninja3 = Ninja.objects.create(first_name="Mel", last_name="Lee", dojo=first_dojo)

In [28]: second_dojo = Dojo.objects.get(id=5)

In [29]: ninja4 = Ninja.objects.create(first_name="john", last_name="bacon", dojo=second_dojo)

In [30]: ninja5 = Ninja.objects.create(first_name="betty", last_name="johnson", dojo=second_dojo)

In [31]: ninja6 = Ninja.objects.create(first_name="Michael", last_name="kors", dojo=second_dojo)

In [32]: third_dojo = Dojo.objects.get(id=6)

In [33]: ninja7 = Ninja.objects.create(first_name="Jenny", last_name="craig", dojo=third_dojo)

In [34]: ninja8= Ninja.objects.create(first_name="Denny", last_name="berger", dojo=third_dojo)

In [35]: ninja98= Ninja.objects.create(first_name="Faith", last_name="berger", dojo=third_dojo)

In [36]: Dojo.objects.first()
Out[36]: <Dojo: Dojo object>

In [37]: Ninja.dojo.ninjas.all()
---------------------------------------------------------------------------
AttributeError                            Traceback (most recent call last)
<ipython-input-37-041b87f3ef1f> in <module>()
----> 1 Ninja.dojo.ninjas.all()

AttributeError: 'ForwardManyToOneDescriptor' object has no attribute 'ninjas'

In [38]: Ninja.dojo(id = 1).all()
---------------------------------------------------------------------------
TypeError                                 Traceback (most recent call last)
<ipython-input-38-01095a87d558> in <module>()
----> 1 Ninja.dojo(id = 1).all()

TypeError: 'ForwardManyToOneDescriptor' object is not callable

In [39]: Dojo.objects.first().ninjas.all()
Out[39]: <QuerySet [<Ninja: Ninja object>, <Ninja: Ninja object>, <Ninja: Ninja object>]>

In [40]: Dojo.objects.last().ninjas.all()
Out[40]: <QuerySet [<Ninja: Ninja object>, <Ninja: Ninja object>, <Ninja: Ninja object>]>

In [41]: Dojo.objects.last().ninjas.all().__dict__
Out[41]:
{'_db': None,
 '_fields': None,
 '_for_write': False,
 '_hints': {'instance': <Dojo: Dojo object>},
 '_iterable_class': django.db.models.query.ModelIterable,
 '_known_related_objects': {<django.db.models.fields.related.ForeignKey: dojo>: {6: <Dojo: Dojo object>}},
 '_prefetch_done': False,
 '_prefetch_related_lookups': (),
 '_result_cache': None,
 '_sticky_filter': False,
 'model': apps.dojo_ninjas.models.Ninja,
 'query': <django.db.models.sql.query.Query at 0x803bf28>}

In [42]: exit()

C:\Users\TL\Documents\python_stack\django\users>python manage.py makemigrations
You are trying to add a non-nullable field 'desc' to dojo without a default; we can't do that (the database needs something to populate existing rows).
Please select a fix:
 1) Provide a one-off default now (will be set on all existing rows with a null value for this column)
 2) Quit, and let me add a default in models.py
Select an option: 1
Please enter the default value now, as valid Python
The datetime and django.utils.timezone modules are available, so you can do e.g. timezone.now
Type 'exit' to exit this prompt
>>> Hello there
Invalid input: unexpected EOF while parsing (<string>, line 1)
>>> "hello there"
Migrations for 'dojo_ninjas':
  apps\dojo_ninjas\migrations\0002_dojo_desc.py
    - Add field desc to dojo

C:\Users\TL\Documents\python_stack\django\users>python manage.py makemigrations
No changes detected

C:\Users\TL\Documents\python_stack\django\users>python manage.py migrate


In [1]: from apps.dojo_ninjas.models import *

In [2]: Dojo.objects.all()[0]
Out[2]: <Dojo: Coding Dojo SV>

In [3]: Dojo.objects.all()[0].name
Out[3]: u'Coding Dojo SV'

In [4]: Dojo.objects.all()[0].city
Out[4]: u'Mountain View'

In [5]: Dojo.objects.all()[0].dojo
---------------------------------------------------------------------------
AttributeError                            Traceback (most recent call last)
<ipython-input-5-8eb9c68dfacc> in <module>()
----> 1 Dojo.objects.all()[0].dojo

AttributeError: 'Dojo' object has no attribute 'dojo'

In [6]: Dojo.objects.all()[0].dojo.ninjas
---------------------------------------------------------------------------
AttributeError                            Traceback (most recent call last)
<ipython-input-6-aee7eba4ac59> in <module>()
----> 1 Dojo.objects.all()[0].dojo.ninjas

AttributeError: 'Dojo' object has no attribute 'dojo'

In [7]: Ninja.objects.all()[0].dojo
Out[7]: <Dojo: Coding Dojo SV>

In [8]: Ninja.objects.all()[0].dojo.city
Out[8]: u'Mountain View'

In [9]: Dojo.objects.all()[0].name
Out[9]: u'Coding Dojo SV'

In [10]: Ninja.objects.all()[0].dojo
Out[10]: <Dojo: Coding Dojo SV>

In [11]: Dojo.objects.all()[0].ninjas.all()
Out[11]: <QuerySet [<Ninja: Ninja object>, <Ninja: Ninja object>, <Ninja: Ninja object>]>

In [12]: Dojo.objects.all()[0].ninjas.all()[0]
Out[12]: <Ninja: Ninja object>

In [13]: Dojo.objects.all()[0].ninjas.all()[0].__dict__
Out[13]:
{'_dojo_cache': <Dojo: Coding Dojo SV>,
 '_state': <django.db.models.base.ModelState at 0x7cf5ef0>,
 'created_at': datetime.datetime(2018, 3, 17, 21, 12, 20, 26000, tzinfo=<UTC>),
 'dojo_id': 4,
 'first_name': u'Ting',
 'id': 3,
 'last_name': u'Lee',
 'updated_at': datetime.datetime(2018, 3, 17, 21, 12, 20, 26000, tzinfo=<UTC>)}
