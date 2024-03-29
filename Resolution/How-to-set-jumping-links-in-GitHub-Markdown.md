## Resolution: How to set jumping links in GitHub Markdown

### Scenario 1: Intra-file

You can link headings simply as follows:

```python
[Description](#NAME-OF-HEADING)
```

**Note:** if the name of the heading has more than one word, join words with `-` (which is essential).

#### Example

The contents below simulate a realistic format, as expected.

<br>

---

## Contents

- [Shining Watermelon](#Shining-Watermelon)
  - [Description from IMDb](#Description-from-IMDb)
  - [Introduction from Wikipedia](#Introduction-from-Wikipedia)
  - [Abstract from Douban](#Abstract-from-Douban)

```python
- [Shining Watermelon](#Shining-Watermelon)
    - [Description from IMDb](#Description-from-IMDb)
    - [Introduction from Wikipedia](#Introduction-from-Wikipedia)
    - [Abstract from Douban](#Abstract-from-Douban)
```

**Note:** `Ctrl` + `left_click` will bring you a smooth trip if you are using Markdown editor like Typora.

<br>

<br>

<br>

*Several empty lines assure apparent responses. (just for illustration)*

<br>

<br>

<br>

## Shining Watermelon

### [Description from IMDb](https://www.imdb.com/title/tt27446493/)

**IMDb rating: 8.9/10 (4.1k)**

> Shining Watermelon (Sparkling Watermelon) will tell the story of a boy living a double life between a model student and a band member who gets to time slip and meets his 18-year-old father. The two will build friendships there.

### [Introduction from Wikipedia](https://en.wikipedia.org/wiki/Twinkling_Watermelon)

> Twinkling Watermelon is a 2023 South Korean television series directed by Son Jong-hyun, and starring Ryeoun, Choi Hyun-wook, Seol In-ah and Shin Eun-soo. It aired on tvN from September 25 to November 14, 2023, every Monday and Tuesday at 20:50 (KST) for 16 episodes. It is also available for streaming on Viu and Viki in selected regions.

### [Abstract from Douban](https://movie.douban.com/subject/36117731/)

**Douban rating: 8.8/10 (4.3k)**

>  (Written in Chinese)
>
> 该剧讲述具有音乐天赋的少年通过一家可疑的乐器店，迫降在陌生的空间，在那里遇到可疑的年轻人们一起组成了乐队"Water Melon Sugar"，而展开的幻想青春剧。

<br>

As far as I am concerned, the plots therein are much better than introduced. It is exciting and worth watching.

<br>

---

### Scenario 2: Inter-file

The trip between files in the repository (project) starts with the root directory, staying with other tips as mentioned above.

```python
# Trip to a specific directory
[Description](/directory)
# Trip to a specific file in the root directory
[Description](/file)
# Trip to a specific file NOT in the root directory
[Description](/directory/file)
# Trip to a specific heading of a file (two cases as mentioned above)
[Description](/file/#NAME-OF-HEADING)
[Description](/directory/file/#NAME-OF-HEADING)
```

#### Example

Assume that you intend to brose `README.md` of the repository (click this [portal](/README.md)):

```python
[portal](/README.md)
```

