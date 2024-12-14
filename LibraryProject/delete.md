## Delete Operation
```python
book.delete()
try:
    deleted_book = Book.objects.get(title="Nineteen Eighty-Four")
except Book.DoesNotExist:
    print("The book has been deleted.")
