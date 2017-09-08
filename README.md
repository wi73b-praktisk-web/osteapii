# OsteAPI Dokumentation

## Resurser

**GET /cheeses**

Resursen repræsenterer alle oste i kartoteket.
Resursen er formateret på følgende måde:

```JSON
[{
    "varenr": number,
    "navn": string,
    "type": "Blåskimmel",
    "pris": 42.5,
    "antal": 57,
    "beskrivelse": {
    "producent": "St. Clemens",
    "vægt": 300,
    "land": "Danmark",
    "fedtinhold": "35%",
    "smag": "mild",
    "billede": "skimmelblå.jpeg"
}
},{
    ...
}]
```

**GET /cheeses/\<varenummer>**

Resursen repræsenterer en enkelt ost i kartoteket.
Resursen er formateret på følgende måde:

```JSON
{
    "varenr": number,
    "navn": string,
    "type": "Blåskimmel",
    "pris": 42.5,
    "antal": 57,
    "beskrivelse": {
    "producent": "St. Clemens",
    "vægt": 300,
    "land": "Danmark",
    "fedtinhold": "35%",
    "smag": "mild",
    "billede": "skimmelblå.jpeg"
    }
}
```

**POST /login**

Resursens varetager log-ind information og returner et accessToken.
Resursens request body er formateret på følgende måde:

```JSON
{
    "username": string,
    "password": string
}
```

Resursens respons er formateret på følgende måde:

```JSON
{
    "AccessToken": string
}
```

AccessToken er en 512 bit HEX streng, generet med randomBytes.


