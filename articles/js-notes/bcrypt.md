# Auth

## bcrypt
Salt is basically a randomly generated string attached to the beginning of the hash in order to make it more resistant to brute-force.

## jwt
The token is not encrypted, so you can extract any data from it, but the digital signature attached to the end of the token can be checked only server-side with a special secret string.
Use [https://jwt.io](https://jwt.io) to know more.

