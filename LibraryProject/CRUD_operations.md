# CRUD Operations for Book Model

## Create Operation
```python
book = Book.objects.create(title="1984", author="George Orwell", publication_year=1949)
retrieved_book = Book.objects.get(title="1984")
print(retrieved_book.title)
print(retrieved_book.author)
print(retrieved_book.publication_year)
book.title = "Nineteen Eighty-Four"
book.save()
updated_book = Book.objects.get(title="Nineteen Eighty-Four")
print(updated_book.title)
book.delete()
try:
    deleted_book = Book.objects.get(title="Nineteen Eighty-Four")
except Book.DoesNotExist:
    print("The book has been deleted.")
