# Belajar-RESTful-API-untuk-Pemula

Architectural Constraints

1. Client–server
2. Stateless
3. Cacheable
4. Uniform interface
5. Layered system
6. Code on demand

Response Status : 

Selalu gunakan response status code yang sesuai dengan Standarisasi HTTP 
Misal jika sukses, gunakan Response Status 2xx
Jika data yang dikirim oleh client tidak valid, gunakan 4xx
Jika terjadi masalah di Server, gunakan 5xx


Contoh Authentication & Authorization
Basic Auth
API-Key
Oauth 2
dan lain-lain


HATEOAS :

HATEOAS singkatan dari Hypermedia as the Engine of Application State
Hypermedia artinya content yang memiliki link menuju resource yang ada


Level Zero

One URL, One HTTP Method
Pada level zero, biasanya Web Service dibuat hanya menggunakan satu URL dan Satu HTTP Method
Contoh adalah SOAP dan XML-RPC, biasanya hanya menggunakan satu URL dan HTTP Method POST saja untuk semua API
Jika kita masih menggunakan teknik seperti ini, artinya kita masih berada di Level Zero

Level One

Many URLs, One HTTP Method
Jika kita sudah menggunakan banyak URL ketika membuat Web Service, namun masih selalu menggunakan satu HTTP Method, maka kita berada di Level One
Biasanya Web Service versi lama masih menggunakan format seperti ini, walaupun sudah menggunakan banyak URL, namun hanya menggunakan satu HTTP Method, biasanya menggunakan POST

Level Two

Many URLs, Each Supporting Multiple HTTP Methods
Ini adalah level dinama kebanyakan Web Service saat ini
Banyak URL, dan tiap URL biasanya mendukung satu atau lebih jenis HTTP Method
Misal url yang sama, menggunakan GET untuk mengambil data, dan POST untuk menambah  data
Jika kita sudah melakukan hal ini, artinya kita sudah berada di Level Two


Level Three

Resources describe their own capabilities and interconnections
Level Three atau paling tinggi sebenarnya mirip dengan Level Two, yang membedakan adalah pada Level Threee setiap resource akan memberikan detail relasi ke resource lainnya, atau singkatnya adalah sudah mengimplementasikan HATEOAS
Memang Level Three ini agak menyulitkan ketika diimplementasikan, dan kebanyakan programmer hanya  berhenti  di Level Two
Dengan mengimplementasikan HATEOAS, kita bisa dengan mudah mendapat URL resource ke relasi data yang kita butuhkan


