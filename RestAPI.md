# Rest API
Welcome to the Rest API documentation of  AnimeShooter.com

## Account

Account API, authentication is done through the `Authorization` header.

| Type |    Action    |      Protection      | Description |
|:----:|:------------:|:--------------------:|:------------|
| POST | ``api/user/regiser`` | None (captcha) | Send json with `Username`, `Email`, `Password` to create an account. |
| POST | ``api/user/login`` | None (captcha) | Send JSON `Username` and `Password` to create a authentication token. |
| POST | ``api/user/update`` | Auth Token | Send JSON `Password` to update your password. |
| GET | ``api/user/info`` | Auth Token | Obtains information about your player. |

## Open 

Open Rest API to obtain information about the game.

| Type |    Action    |      Protection      | Description |
|:----:|:------------:|:--------------------:|:------------|
| GET | ``api/player/online`` | None | Obtain a list of currently logged in players. |
| GET | ``api/player/{id}`` | None | Obtain information about the selected player. |
| GET | ``api/leaderboard`` | None | Get the current leaderboard. |
| GET | ``api/room/`` | None | Get a list of currently available game rooms. |


### Misc
Misc, a list of stuff that might come in handy.

| Type |    Action    |      Protection      | Description |
|:----:|:------------:|:--------------------:|:------------|
| GET | ``api/img/level/{lvl}`` | None | Get the PNG of the requested level. |
| GET | ``api/img/maps/small/{name}`` | None | Get the PNG of the request map *(by name or id)* |
