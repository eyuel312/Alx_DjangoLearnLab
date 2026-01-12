from bookshelf.models import Book
book = Book.objects.create(title="1984", author="George Orwell", publication_year=1949)
print(book)
# Expected Output: 1984
from bookshelf.models import Book
book = Book.objects.get(title="1984")
print(book.title, book.author, book.publication_year)
# Expected Output: 1984 George Orwell 1949
from bookshelf.models import Book
book = Book.objects.get(title="1984")
book.title = "Nineteen Eighty-Four"
book.save()
print(book.title)
# Expected Output: Nineteen Eighty-Four
from bookshelf.models import Book
book = Book.objects.get(title="Nineteen Eighty-Four")
book.delete()
# Expected Output: (1, {'bookshelf.Book': 1})
print(Book.objects.all())
# Expected Output: <QuerySet []>
