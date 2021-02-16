# graphene-tutorial

Python Graphene Tutorial - Cookbook

---

Settings

```shell
python manage.py migrate

python manage.py loaddata ingredients
```

Try to send query in http://localhost:8000/graphql

```graphql
query {
  allIngredients {
    id
    notes
    category {
      id
      name
    }
  }
  categoryByName(name: "Meat") {
    id
    name
    ingredients {
      name
    }
  }
}
```
