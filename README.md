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
  allIngredients(first: 3) {
    pageInfo {
      hasNextPage
      hasPreviousPage
      startCursor
      endCursor
    }
    edges {
      node {
        id
        name
      }
      cursor
    }
  }
  allCategories(
    ingredients: ["SW5ncmVkaWVudE5vZGU6MQ==", "SW5ncmVkaWVudE5vZGU6Mw=="]
  ) {
    edges {
      node {
        id
        name
      }
    }
  }
  ingredient(id: "SW5ncmVkaWVudE5vZGU6MQ==") {
    id
    name
  }
}
```
