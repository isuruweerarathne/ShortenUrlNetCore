# ASP.NET Core MVC URL Shortener
A basic implementation of an URL shortener web application using ASP.NET Core MVC and Entity Framework Core.


# Algorithm

So, how works an URL shortener?

Basicaly, we store the URL in database, so it has a numeric ID, an we convert it to a another base in order to have a "stringified" version of the ID.

When we have the short URL the process is:
- convert the "stringified" ID to the numeric ID.
- load the data from DB.
- redirect to the original URL using an HTTP redirection.


## Implementation

I've used the ShortURL class by delight.im to encode the longUrl and again decode when we are retrieving.

## Usage

First,  type `dotnet restore` in order to retrieve the dependancies of the project.

In order to init the DB schema, you have to rune the command `dotnet-ef database update`.

Then, simply type `dotnet run` on your command prompt and then browse to http://localhost:5001.
