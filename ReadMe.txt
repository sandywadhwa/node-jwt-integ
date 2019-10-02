// LOGIN CALL - FAILING
curl -X POST -H "Content-Type: application/json" -d '{"username": "beingzero", "password": "beingzero"}' http://localhost:8000/login

// LOGIN CALL - PASSING
curl -X POST -H "Content-Type: application/json" -d '{"username": "admin", "password": "password"}' http://localhost:8000/login

// GET CALL without TOKEN - FAILING
curl -X GET -H "Content-Type: application/json" http://localhost:8000

// GET CALL with TOKEN - PASSING (Bearer token in authorization header)
curl -X GET -H "authorization: Bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJ1c2VybmFtZSI6ImFkbWluIiwiaWF0IjoxNTY5OTgxNTEwLCJleHAiOjE1NzAwNjc5MTB9.dpUXzPVXWSjCLpjft2TgNv8jZW-LV4nBYUSfB7SrSyk" -H "Content-Type: application/json" http://localhost:8000

// GET CALL with TOKEN - PASSING (token in authorization header)
curl -X GET -H "authorization: eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJ1c2VybmFtZSI6ImFkbWluIiwiaWF0IjoxNTY5OTgxNTEwLCJleHAiOjE1NzAwNjc5MTB9.dpUXzPVXWSjCLpjft2TgNv8jZW-LV4nBYUSfB7SrSyk" -H "Content-Type: application/json" http://localhost:8000

// GET CALL with TOKEN - PASSING (token in x-access-token header)
curl -X GET -H "x-access-token: eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJ1c2VybmFtZSI6ImFkbWluIiwiaWF0IjoxNTY5OTgxNTEwLCJleHAiOjE1NzAwNjc5MTB9.dpUXzPVXWSjCLpjft2TgNv8jZW-LV4nBYUSfB7SrSyk" -H "Content-Type: application/json" http://localhost:8000

// GET CALL with TOKEN - PASSING (Bearer token in x-access-token header)
curl -X GET -H "x-access-token: Bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJ1c2VybmFtZSI6ImFkbWluIiwiaWF0IjoxNTY5OTgxNTEwLCJleHAiOjE1NzAwNjc5MTB9.dpUXzPVXWSjCLpjft2TgNv8jZW-LV4nBYUSfB7SrSyk" -H "Content-Type: application/json" http://localhost:8000
