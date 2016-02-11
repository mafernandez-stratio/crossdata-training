# crossdata-training

curl -XGET 'http://localhost:9200/_nodes?pretty=true'

curl -XGET 'http://localhost:9200/_cluster/health?pretty=true'

curl -XPUT 'http://localhost:9200/company/clerk/1' -d '
{
    "number": 212,
    "name": "Mike",
    "surname": "Miller",
    "age": 29,
    "salary": 32000,
    "experience": 5,
    "speciality": "shoes"
}'

curl -XPUT 'http://localhost:9200/company/clerk/2' -d '
{
    "number": 94,
    "name": "Laura",
    "surname": "Smith",
    "age": 34,
    "salary": 34000,
    "experience": 10,
    "speciality": "make-up"
}'

curl -XPUT 'http://localhost:9200/company/clerk/3' -d '
{
    "number": 158,
    "name": "Steve",
    "surname": "Jones",
    "age": 45,
    "salary": 38000,
    "experience": 19,
    "speciality": "televisions"
}'

curl -XPUT 'http://localhost:9200/company/clerk/4' -d '
{
    "number": 120,
    "name": "Liam",
    "surname": "Moore",
    "age": 32,
    "salary": 29000,
    "experience": 7,
    "speciality": "motorbikes"
}'

curl -XPUT 'http://localhost:9200/company/clerk/5' -d '
{
    "number": 204,
    "name": "Emma",
    "surname": "Davis",
    "age": 24,
    "salary": 24000,
    "experience": 1,
    "speciality": "books"
}'

curl -XGET 'http://localhost:9200/company/clerk/_search?pretty=true'




