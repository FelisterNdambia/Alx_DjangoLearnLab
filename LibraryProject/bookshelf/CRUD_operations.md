# Create Operation for Book Model

## command
from bookshelf.models import Book
book = Book.objects.create(title="1984", author="George Orwell", publication_year=1949)
book
## Output
Book: 1984 by George Orwell (1949)

# retrive operations
## command
Book.objects.get(id=book.id)
## Output
Book: 1984 by George Orwell (1949)

# Update operations
## command
book.title = "Nineteen Eighty-Four"
book.save()
book
## Output
Book: Nineteen Eighty-Four by George Orwell (1949)

# delete operations
## command
book.delete()
Book.objects.all()
## output
QuerySet []