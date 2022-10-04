# ![gollum](https://user-images.githubusercontent.com/20764455/193718827-73c4542b-f89a-4fff-8fc2-49171985aae4.gif) LOTR SDK Design 

This SDK will let developers search for information using THE ONE API. Developers can use this SDK to look up books, characters, quotes, and movies. The get method can get all or a specific object by id. 


## :mage_man: Instructions:


These are the following steps to use this SDK: 

:white_small_square: 1. Open your Comand Prompt 

:white_small_square: 2. Go to the directory you would like to install the package. 

:white_small_square: 3. Create a virtual environment: 
	for Windows type:
```
py -m venv EnvironmentName
```
:white_small_square: 4. Activate the environment 
	type:
```
EnvironmentName\Scripts\activate
```

:white_small_square: 5. Install requests in your environment: 
	for Windows type:
```
pip install requests
```
:white_small_square: 6. Hurry! Now lets install the SDK package. 
	type:
```	
pip install Gian-lotr
```

:white_small_square: 7. Lets code some python
	type:
```
python
```
:white_small_square: 8. Cograts! Now lets import TestingClient 
	type:
```
from Gian_lotr.rest import TestingClient
```
:white_small_square: 9. Lets create a client 
	type:
```
client = TestingClient(location="lotr")
```
:white_small_square: 10. Let's see all the movies: 
	type:
```	
client.movie.get()
```
:white_small_square: 11. Lets find a movie by id 
	type:
```
client.movie.get(object_id="5cd95395de30eff6ebccde56")
```	

This SDK will let developers search for information using THE ONE API. Developers can use this SDK to look up books, characters, quotes, and movies. The get method can get all or a specific object by id. 


## :deciduous_tree:	 File Structure: 

FolderInstalledGian-SDK\Lib\site-packages\Gian_lotr
```
Gian_lotr/
└── rest/
    └── book/
        ├── __init__.py
    └── character/
        ├── __init__.py
    └── movie/
        ├── __init__.py
    └── quote/
        ├── __init__.py
    └── __init__.py
       	

```

In the __init__ for the rest folder, you will find a class() with a few methods. The purpose of this class is to create an object that can contain different information. This will come in handy when adding various API endpoints or filtering information. This file also contains an APIRequester class for different APIs and a PathBuilder class to create more complex Strings in the future.  

The book, character, movie, and quote folder contain an __init__ file as well. Each one creates an object of a different class. 


## 	:bow_and_arrow: Details: 

The first step is to create a client object with the name of the location of the API. At the moment "lotr" (https://the-one-api.dev/v2/) is the only API endpoint that is being used. However, this application is designed to add many APIs very easily. 

```
Example: 

name of object           variable name 
  |      initialize class   |     name of API
            |               |      |
client = TestingClient(location="lotr")
```



Then what type of information is going to be retrieved such as a book or quote. After, add the get() or get(object_id="ID HERE") to find the right information.   

```
Example: 

object      method 
  | location |          id
        |               |
client.movie.get(object_id="ID here") 

```

## :dagger: Other Examples: 

client.book.get(object_id ="5cf5805fb53e011a64671582")

client.book.get()

client.charater.get()

client.quote.get()
  
