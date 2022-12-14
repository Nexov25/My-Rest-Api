# ```Alphabot-Api```
<p align="center">
<a href="https://github.com/AkiRaID/followers"><img title="Followers" src="https://img.shields.io/github/followers/AkiRaID?color=red&style=flat-square"></a>
<a href="https://github.com/AkiRaID/Akira-rest-api/stargazers/"><img title="Stars" src="https://img.shields.io/github/stars/AkiRaID/Akira-rest-api?color=blue&style=flat-square"></a>
<a href="https://github.com/AkiRaID/Akira-rest-api/network/members"><img title="Forks" src="https://img.shields.io/github/forks/AkiRaID/Akira-rest-api?color=red&style=flat-square"></a>
<a href="https://github.com/AkiRaID/Akira-rest-api/watchers"><img title="Watching" src="https://img.shields.io/github/watchers/AkiRaID/Akira-rest-api?label=Watchers&color=blue&style=flat-square"></a>
<a href="https://github.com/AkiRaID/Akira-rest-api"><img title="Open Source" src="https://badges.frapsoft.com/os/v2/open-source.svg?v=103"></a>
<a href="https://github.com/AkiRaID/Akira-rest-api/"><img title="Size" src="https://img.shields.io/github/repo-size/AkiRaID/Akira-rest-api?style=flat-square&color=green"></a>
<a href="https://hits.seeyoufarm.com"><img src="https://hits.seeyoufarm.com/api/count/incr/badge.svg?url=https%3A%2F%2Fgithub.com%2FAkiRaID%2FAkira-rest-api&count_bg=%2379C83D&title_bg=%23555555&icon=probot.svg&icon_color=%2300FF6D&title=hits&edge_flat=false"/></a>
<a href="https://github.com/AkiRaID/Akira-rest-api/graphs/commit-activity"><img height="20" src="https://img.shields.io/badge/Maintained%3F-yes-green.svg"></a>&nbsp;&nbsp;
</p>
<p align='center'>
    </p>

-------
<h1 align="center">Assalamu'alaikum <img src="https://user-images.githubusercontent.com/1303154/88677602-1635ba80-d120-11ea-84d8-d263ba5fc3c0.gif" width="40px" alt="Hi"><br>I'M Akira๐ </h1>
<p align="center">
  <img src="https://c.top4top.io/p_2069qnvob1.jpg" /></>
</p>

- โ๏ธ My Name is Akira
- ๐  My Real Name is Muhammad Reihan Saputra
- ๐ญ I am not programmer

## ```Connect with me```
<p align="center">
  <a href="https://instagram.com/muhammadreihansaputra27"><img src="https://img.shields.io/badge/Instagram-E4405F?style=for-the-badge&logo=instagram&logoColor=white"/> 
  <a href="https://wa.me/6282158549899"><img src="https://img.shields.io/badge/WhatsApp-25D366?style=for-the-badge&logo=whatsapp&logoColor=white" />
  <a href="https://github.com/AkiRaID"><img src="https://img.shields.io/badge/-GitHub-black?style=flat-square&logo=github" /> 
  <a href="https://m.youtube.com/channel/UCvVd-kAsrJUjg0bwKqxUPeg"><img src="https://img.shields.io/youtube/channel/subscribers/UCvVd-kAsrJUjg0bwKqxUPeg?style=social" /> <br>

</p>

## ```How to install```

[`Click Here For Tutorial`](https://youtu.be/POjBjZx9tvY)<br>

<p align="center">
  <a href="https://youtu.be/POjBjZx9tvY"><img src="https://f.top4top.io/p_207542cfh1.jpg" />
</p>


## ```Api Features```

1. ```๐ฟ๐ค๐ฌ๐ฃ๐ก๐ค๐๐ & ๐๐ค๐๐๐๐ก ๐๐๐๐๐ ๐คณ ```
<details>

<summary> <b>Example Case</b></summary><br/>

```
Example Case:

case 'youtube_audio':  
      if (args.length < 1) return reply("Where's the link bro")
      if (!isUrl(args[0]) && !args[0].includes('youtu')) return reply('```Invalid link```')
      reply(lang.wait()) 
      anu = await fetchJson(`https://api-alphabot.herokuapp.com/api/yutub/audio?url=${args[0]}&apikey=Alphabot`)
        ini_txt = `YT AUDIO HAS BEEN FOUND\n\n`
        ini_txt += `โข Judul : ${anu.result.title}\n`
        ini_txt += `โข Ext : mp3\n`
        ini_txt += `โข Size : ${anu.result.filesize}\n\n_Tunggu beberapa menit video akan segera di kirimkan_`
        ini_txt2 = await getBuffer(anu.result.thumb)
        ini_txt3 = await getBuffer(anu.result.result)
      alpha.sendMessage(from, ini_txt2, image, { quoted: mek, caption: ini_txt })
      alpha.sendMessage(from, ini_txt3, audio, { mimetype: 'audio/mp4', quoted: mek, ptt:true})
      break

```
</details>

2. ```๐๐จ๐ก๐๐ข๐๐ ๐```

<details>

<summary> <b>Example Case</b></summary><br/>

```
Example Case:

case 'hadist_sahih':
      if (args.length < 1) return reply(`Usage: ${prefix + command} kitab|nomor\nExample : ${prefix + command} Bukhari|15`)
      get_args = args.join(" ").split("|")
      kitab = get_args[0]
      nomor = get_args[1]
      var hadist = await fetchJson('https://api-alphabot.herokuapp.com/api/hadits?kitab=${kitab}&nomor=${nomor}&apikey=Alphabot')
      ini_result = hadist.result
         ini_txt = `Name : ${ini_result.name}\n`
         ini_txt += `Id : ${ini_result.id}\n`
         ini_txt += `Available : ${ini_result.availabel}\n`
         ini_txt += `Number : ${ini_result.contents.number}\n`
         ini_txt += `Arab : ${ini_result.contents.arab}\n`
         ini_txt += `Ind : ${ini_result.contents.id}`
      reply(ini_txt)
      break
```

</details>

3. ```๐๐ข๐๐๐๐จ ๐ผ๏ธ```

<details>

<summary> <b>Example Case</b></summary><br/>


```
Example Case:

case 'wallpaper_programming':
     get_result = await fetchJson(`https://api-alphabot.herokuapp.com/api/wallpaper/teknologi?apikey=Alphabot`)
     get_result = get_result.result
     for (var x = 0; x <= 5; x++) {
     var ini_buffer = await getBuffer(get_result[x])
     await alpha.sendMessage(from, ini_buffer, image)
     }
     break

```
</details>

4. ```๐๐๐ฃ๐๐ค๐ข โ```

<details>

<summary> <b>Example Case</b></summary><br/>

```
Example Case:

case 'random_quote':
     ini_result = await fetchJson('https://api-alphabot.herokuapp.com/api/randomquote?apikey=Alphabot')
     get_result = ini_result.result
        ini_txt = `${get_result.quotes}\n\n`
       ini_txt += `~ ${get_result.author}`
     reply(ini_txt)

```
</Details>

5. ```๐๐๐ญ๐ฉ ๐๐๐ ๐๐ง 2๐ฟ ๐ฉโโค๏ธโ๐โ๐ฉ```

<details>

<summary> <b>Example Case</b></summary><br/>

```
Example Case:

case 'maker_2d':
      if (args.length < 1) return reply(`Usage: ${prefix + command} teks\nExample : ${prefix + command} AkiRaID)
      teksnya = args.join(" ")
      ini_result = await fetchJson(`https://api-alphabot.herokuapp.com/api/maker?text=${teksnya}&apikey=Alphabot`}
      get_result = ini_result.result
         ini_img = await getBuffer(get_result.results)
      alpha.sendMessage(from, ini_img, image,{quoted :mek, caption : 'Nih kak hasilnya'})
      break
```
</Details>

6. ```๐๐๐ญ๐ฉ ๐๐๐ ๐๐ง 3๐ฟ ๐ซ```

<details>

<summary> <b>Example Case</b></summary><br/>

```
Example Case:

case 'maker_3d':
      if (args.length < 1) return reply(`Usage: ${prefix + command} teks\nExample : ${prefix + command} AkiRaID)
      teksnya = args.join(" ")
      ini_result = await fetchJson(`https://api-alphabot.herokuapp.com/api/maker3d?text=${teksnya}&apikey=Alphabot`}
      get_result = ini_result.result
         ini_img = await getBuffer(get_result.results)
      alpha.sendMessage(from, ini_img, image,{quoted :mek, caption : 'Nih kak hasilnya'})
      break
```
</Details>

7. ```๐๐๐ญ๐ฉ ๐๐๐ ๐๐ง ๐๐ฉ๐๐๐ง๐จ ๐พ```

<details>

<summary> <b>Example Case</b></summary><br/>

```
Example Case:

case 'sertifikat_ff':
      if (args.length < 1) return reply(`Usage: ${prefix + command} teks\nExample : ${prefix + command} AkiRaID)
      teksnya = args.join(" ")
      ini_result = await fetchJson(`api-alphabot.herokuapp.com/api/maker/special/epep?text=${teksnya}&apikey=Alphabot`}
      get_result = ini_result.result
         ini_img = await getBuffer(get_result.results)
      alpha.sendMessage(from, ini_img, image,{quoted :mek, caption : 'Nih kak hasilnya'})
      break
```
</Details>

8. ```๐๐๐ค๐ฉ๐ค๐ค๐ญ๐ฎ ๐```

<details>

<summary> <b>Example Case</b></summary><br/>

```
Example Case:

case 'coffe_cup':
      if (args.length < 1) return reply(`Usage: ${prefix + command} teks\nExample : ${prefix + command} AkiRaID)
      teksnya = args.join(" ")
      ini_result = await fetchJson(`https://percobaannih.herokuapp.com/api/textmaker/senja?text=${teksnya}&theme=coffee-cup&apikey=Alphabot`}
      get_result = ini_result.result
         ini_img = await getBuffer(get_result.url)
      alpha.sendMessage(from, ini_img, image,{quoted :mek, caption : 'Nih kak hasilnya'})
      break
```
</Details>

9. ```๐ผ๐ฃ๐๐ข๐ ๐```

<details>

<summary> <b>Example Case</b></summary><br/>

```
Example Case:

case 'manga':
      if (args.length < 1) return reply(`Example : ${prefix + command} naruto`)
      query = args.join(" ")
      var manga = await fetchJson('https://percobaannih.herokuapp.com/api/anime/kusonime?search=${query}&apikey=Alphabot')
      ini_result = manga.result
         ini_txt = `Title : ${ini_result.title}\n`
         ini_txt += `Title Japan : ${ini_result.title_jp}\n`
         ini_txt += `Genre : ${ini_result.genre}\n`
         ini_txt += `Season : ${ini_result.season}\n`
         ini_txt += `Producer : ${ini_result.producer}\n`
         ini_txt += `Type : ${ini_result.contents.number}\n`
         ini_txt += `Status : ${ini_result.availabel}\n`
         ini_txt += `Total Episode : ${ini_result.contents.number}\n`
         ini_txt += `Score : ${ini_result.contents.arab}\n`
         ini_txt += `Duration : ${ini_result.availabel}\n`
         ini_txt += `Release : ${ini_result.contents.number}\n`
         ini_txt += `Description : ${ini_result.contents.arab}`
         ini_txt2 = await getBuffer(ini_result.thumb)
      reply(ini_txt)
      break
```
</Details>

10. ```๐ผ๐จ๐ช๐ฅ๐๐ฃ ๐๐๐ข๐๐ก๐๐ฃ๐ ๐ฝ๏ธ```

<details>

<summary> <b>Example Case</b></summary><br/>

```
Example Case:

case 'asupan_santuy':
     ini_result = await fetchJson(`https://api-alphabot.herokuapp.com/api/asupan/santuy?apikey=Alphabot`)
     get_result = ini_result.result
        ini_vid = await getBuffer(get_result.url)
     alpha.sendMessage(from, ini_vid, video, {mimetype: 'video/mp4',quoted:mek})
     break

```
</Details>

11. ```๐๐๐๐ ๐```

<details>

<summary> <b>Example Case</b></summary><br/>

```
Example Case:

case 'nsfw_ass':
     ini_result = await fetchJson(`https://api-alphabot.herokuapp.com/api/nsfw/ass?apikey=Alphabot`)
     get_result = ini_result.result
        ini_img = await getBuffer(get_result)
     alpha.sendMessage(from, ini_img, image, {quoted:mek})
     break

```
</Details>

12. ```๐๐๐ข๐๐จ ๐ฎ```

<details>

<summary> <b>Example Case</b></summary><br/>

```
Example Case:

Untuk game memerlukan function jadi gua gk kasi example dulu

```
</Details>

13. ```๐๐๐๐๐ ๐พ๐๐ฌ๐ ๐ญ```

<details>

<summary> <b>Example Case</b></summary><br/>

```
Example Case:

case 'cewe_vietnam':
     ini_result = await fetchJson(`https://api-alphabot.herokuapp.com/api/cewe/vietnam?apikey=Alphabot`)
     get_result = ini_result.result
        ini_img = await getBuffer(get_result.url)
     alpha.sendMessage(from, ini_img, image, {quoted:mek})
     break

```
</Details>

14. ```๐๐๐ก๐ข๐ผ๐ฅ๐๐  ๐ฌ```

<details>

<summary> <b>Example Case</b></summary><br/>

```
Example Case:

case 'cari_film':
      if (args.length < 1) return reply(`Example : ${prefix + command} Avengers)
      query = args.join(" ")
      get_result = await fetchJson(`https://api-alphabot.herokuapp.com/api/filmapik/search?film=${query}&apikey=Alphabot`)
      for (var x = 0; x <= 1; x++) {
         ini_img = get_result[x].result.thumbnailPotrait
         ini_txt = `DATA BERHASIL DI TEMUKAN\n\n`
         ini_txt += ` Title : ${get_result[x].result.title}\n`
         ini_txt += `Rating :get_result[x].result.rating\n`
         ini_txt += `Episode : get_result[x].result.episode\n`
         ini_txt += `Id : get_result[x].result.movieId
         ini_txt += `Views : get_result[x].result.datails.views
         ini_txt += `Genre :get_result[x].result.datails.genre\n`
         ini_txt += `Duration :get_result[x].result.datails.duration\n`
         ini_txt += `Release :get_result[x].result.datails.release\n`
         ini_txt += `Total Eps. :get_result[x].result.datails.totalEpisodes\n`
         ini_txt += `Description :get_result[x].result.datails.description`
      await alpha.sendMessage(from, ini_img, image, {caption: ini_txt, quoted : mek})
      }
      break

```
</Details>

15. ```๐๐ 21 ๐ฆ```

<details>

<summary> <b>Example Case</b></summary><br/>

```
Example Case:

case 'lk21_tahun': //mencari film lk21 berdasarkan tahun
      if (args.length < 1) return reply(`Usage : ${prefix + command} Tahun\nExample : ${prefix + command} 2021)
      query = args.join(" ")
      get_result = await fetchJson(`https://api-alphabot.herokuapp.com/api/lk21/year?tahun=${query}&apikey=Alphabot`)
      for (var x = 0; x <= 1; x++) {
         ini_img = get_result[x].result.result.thumbnail
         ini_txt = `DATA BERHASIL DI TEMUKAN\n\n`
         ini_txt += `Title : ${get_result[x].result.result.title}\n`
         ini_txt += `Rating :get_result[x].result.result.rating\n`
         ini_txt += `Genre :get_result[x].result.result.genre\n`
         ini_txt += `Duration :get_result[x].result.result.duration\n`
         ini_txt += `Quality :get_result[x].result.result.quality\n`
         ini_txt += `Trailer :get_result[x].result.result.trailer\n`
         ini_txt += `Watch :get_result[x].result.result.watch`
      await alpha.sendMessage(from, ini_img, image, {caption: ini_txt, quoted : mek})
      }
      break
```
</Details>

16. ```๐๐๐ฌ๐จ ๐ฐ```

<details>

<summary> <b>Example Case</b></summary><br/>

```
Example Case:

case 'republika': 
      if (args.length < 1) return reply(`Usage : ${prefix + command} jenis berita\nExample : ${prefix + command} ekonomi)
      query = args.join(" ")
      get_result = await fetchJson(`https://api-alphabot.herokuapp.com/api/news/republika?type=${query}&apikey=Alphabot`)
      for (var x = 0; x <= 1; x++) {
         ini_txt = `DATA BERHASIL DI TEMUKAN\n\n`
         ini_txt += `Title : ${get_result[x].result.data.title}\n`
         ini_txt += `Link :get_result[x].result.data.link\n`
         ini_txt += `Isodate :get_result[x].result.data.isoDate\n`
         ini_txt += `Kategori :get_result[x].result.data.categories\n`
         ini_txt += `Creator :get_result[x].result.data.creator\n`
         ini_txt += `Description :get_result[x].result.data.description`
      reply(ini_txt)
      }
      break

```
</Details>

17. ```๐๐ฃ๐๐ค๐๐ & ๐ฟ๐๐๐ค๐๐ ๐จโ๐ป```

<details>

<summary> <b>Example Case</b></summary><br/>

```
Example Case:

case 'base64encode':
      if (args.length < 1) return reply(`Usage : ${prefix + command} teks\nExample : ${prefix + command} AkiRaID)
      query = args.join(" ")
      ini_result = await fetchJson(`https://api-alphabot.herokuapp.com/api/base?apikey=Alphabot&type=base64&encode=${query}`)
      get_result = ini_result.result
         ini_txt = `Type : ${get_result.type}\n`
         ini_txt += `String : ${get_result.string}\n`
         ini_txt += `Encode : ${get_result.encode}`
      reply(ini_txt)
      break
```
</Details>

18. ```๐๐ฉ๐๐๐ง๐จ ๐```

<details>

<summary> <b>Example Case</b></summary><br/>

```
Example Case:

case 'covid_word':
     ini_result = await fetchJson('https://api-alphabot.herokuapp.com/api/covidworld?apikey=Alphabot')
     get_result = ini_result.result
        ini_txt = `C O V I D  W O R L D`
        ini_txt += `Total Case : ${get_result.totalCases}\n`
        ini_txt += `Deaths : ${get_result.deaths}\n`
        ini_txt += `Recovered : ${get_result.recovered}\n`
        ini_txt += `Active Cases : ${get_result.activeCases}\n`
        ini_txt += `Closed Cases : ${get_result.closedCases}\n`
        ini_txt += `lastUpdate : ${get_result.lastUpdate}`
     reply (ini_txt)
     break
```
</Details>

## ```coffee โ```

- [`SAWERIA`](https://saweria.co/Akira27)

## ```Thanks To```

- [`Zahir`]()
- [`Zeeone OFC`]()
