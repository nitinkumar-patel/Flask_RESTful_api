# my_flask_app

Login:
    step1:
        curl -H "Content-Type: application/json" http://localhost:5000/auth -X POST -d '{"username":"nitin","password":"test"}'
    
o/p: 
{
  "access_token": "eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzI1NiJ9.eyJpZGVudGl0eSI6MiwiZXhwIjoxNTIyNTU0MzIxLCJuYmYiOjE1MjI1NTQwMjEsImlhdCI6MTUyMjU1NDAyMX0.qY7dAE-_pjPkC80VmTVuzn48fq1ESAT3EFJTIEZ3nIA"
}
    step2:
        export ACCESS="eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzI1NiJ9.eyJpZGVudGl0eSI6MiwiZXhwIjoxNTIyNTU0MzIxLCJuYmYiOjE1MjI1NTQwMjEsImlhdCI6MTUyMjU1NDAyMX0.qY7dAE-_pjPkC80VmTVuzn48fq1ESAT3EFJTIEZ3nIA"

    step3:
        curl -H "Authorization: JWT $ACCESS" http://localhost:5000/items
