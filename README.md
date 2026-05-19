# TDD with DRF

A project for setting up **Test-Driven Development (TDD)** using Python, Django REST Framework, and PostgreSQL. The domain is a recipe management API, but the focus is on writing tests first and letting them drive the implementation.

## Tech Stack

- **Backend:** Python, Django, Django REST Framework
- **Database:** PostgreSQL
- **Auth:** Token-based authentication
- **API Docs:** drf-spectacular (OpenAPI 3)
- **Containerization:** Docker, Docker Compose
- **CI:** Travis CI

## Test Structure

| Module | Tests cover |
|--------|-------------|
| `core/tests/test_model.py` | User model, email normalization, Recipe/Tag/Ingredient creation, image path generation |
| `core/tests/test_admin.py` | Django admin customization for custom user model |
| `user/tests/test_user_api.py` | Registration, token auth, profile retrieval and update |
| `recipe/tests/test_recipe_api.py` | Full CRUD, filtering by tag/ingredient, image upload |
| `recipe/tests/test_tags_api.py` | Tag listing, update, delete |
| `recipe/tests/test_ingredients_api.py` | Ingredient listing, update, delete |


```bash
docker-compose up
```

The API will be available at `http://localhost:8000`.
API documentation (Swagger UI) is available at `http://localhost:8000/api/docs`.

## Running Tests

```bash
docker-compose run --rm app sh -c "python manage.py test"
```
