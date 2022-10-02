**Localstorage**

1. Localstorage stays even after user closes the browser unlike sessionStorage.
1. Data in storage is stored in key-value pairs as strings. If we try to store arrays it gets convered into string. To use it we may need to parse the data.
1. Methods-
   1. localStorage.setItem("name", "Robert Smith")
   1. localStorage.getItem("name") -  it will return “Robert Smith”
   1. localStorage.removeItem("name")
   1. **localStorage.clear() -** will clear the entire localStorage

