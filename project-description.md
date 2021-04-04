# Project description

As I mentioned during the call, there are two main parts to this project:


## Part 1: Gather all existing videos and drop them into a csv file

Because the format of the titles is not uniform, we will have to cleanup and format some of the data in the title 
manually.  It's virtually impossible to automate everything because of this reason.

The following are the different title formats you will find:

### Type 1:  <REACCION> + <ARTIST> + <HYPHEN> + <SONG TITLE> + <ADDITIONAL INFO IN PARENTHESES>

Examples:  

1. REACCION RAUW ALEJANDRO - YO SABIA
   
<REACCION> + <RAUW ALEJANDRO> + <-> + <YO SABIA>:
   
https://www.youtube.com/watch?v=YrW_Ld8lShc

2. REACCION BHAVI - SUPER SUMO (PROD BY HALPE)
   
<REACCION> + <BHAVI> + <-> + <SUPER SUMO> + <(PROD BY HALPE)>

https://www.youtube.com/watch?v=IAUhCDH1yYg

___

### TYPE 2: <EMOTICON> + <TEXT> + <EMOTICON> + <ARTIST> + <HYPHEN> + <SONG> + <ADDITIONAL INFORMATION>

_Note: Sometimes there's a dot after the emoticon as well_

Examples:


1. :sunglasses: REACCION Y CRITICAS: TRAP :sunglasses:. Arte Elegante & Rdo feat. Chystemc - El Rap nos liberó
   

   <:sunglasses:> + <REACCION Y CRITICAS: TRAP> + <:sunglasses:> + . + <Arte Elegante & Rdo feat. Chystemc> + <-> <El 
   Rap nos liberó>: 
   
https://www.youtube.com/watch?v=8yhHThzZ0fY
   
2. :sunglasses: REACCION Y CRITICA MUSICAL :sunglasses: Congreso - En todas las esquinas - 1989
   
<:sunglasses:> + <REACCION Y CRITICA MUSICAL> + <:sunglasses:> + <Congreso> + <-> + <En todas las esquinas> + <- 1989>

https://www.youtube.com/watch?v=ecX_3FcQp0k&t=11s

___
   
### TYPE 3: <EMOTICON> + <TEXT> + <EMOTICON> + <SONG> + <HYPHEN> + <ARTIST>

:sunglasses: REACCION Y CRITICA MUSICAL :sunglasses: Alturas - Inti Illimani

<:sunglasses:> + <REACCION Y CRITICA MUSICAL> + <:sunglasses:> + <SONG> + <ARTIST>

_As you can see, sometimes the order of artist and song are swapped.  There are even some cases in which the name 
of the artist is in parentheses. We're gonna have to deal with these cases afterwards when we cleanup the csv file_

https://www.youtube.com/watch?v=ImmX_JB0iyQ

https://www.youtube.com/watch?v=qYPyg4DP9L0

___


### TYPE 4: <Lokko: Reaccion a> + <ARTIST> + <HYPHEN> + <SONG> + <ADDITIONAL INFORMATION IN PARENTHESES>

Example:

Lokko: Reacción a Los Jaivas - Los Momentos (de Eduardo Gatti)

<Lokko: Reaccion a> + <Los Jaivas> + <-> + <Los Momentos> + <(de Eduardo Gatti)>

https://www.youtube.com/watch?v=nN3UG_btK_Q

___
___

## Part 2: Automate the updating of one or more Spotify playlists

From now on, all the titles will follow the format in Type 4, i.e. <Lokko: Reaccion a> + <ARTIST> + <HYPHEN> + <SONG> + <ADDITIONAL INFORMATION IN PARENTHESES>

The idea is that, from  now on, every time a new video matching this format is published in the channel, the artist 
and song information are automatically extracted and used for updating one or more Spotify playlists

The process should look something like this:


[A new video is created] :arrow_right: [a script listens to the notification, extracts the data, and sends it to 
spotify or another service] :arrow_right: [The new songs are populated into the pre-defined playlists]

For this part, I have a seedbox where I could put the script, or we could add it as a function on a cloud service, 
or something like that.


The Playlist to be updated is this one: https://open.spotify.com/playlist/0SsJQMbrnw4ze6jfbfFF3f?si=jl4p9zkoQ_K0mDsGTrsfuA

But it should be possible to easily add more playlists if desired.

___

## CSV file format

The csv file should be formatted as [artist, song], like this:

|Artist         |Song         |
|---------------|-------------|
|Michael Jackson|Thriller     |
|Beyonce        |Single Ladies|



   



