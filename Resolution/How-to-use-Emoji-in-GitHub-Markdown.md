## Resolution: How to use Emoji in GitHub Markdown

### Resolution 1 (recommended in HTML)

Represent specific Emoji with UTF-8 decimal (or hexadecimal) encoding; see [here](https://www.w3schools.com/charsets/ref_emoji_smileys.asp) or [here](https://www.quackit.com/character_sets/emoji/emoji_v3.0/unicode_emoji_v3.0_characters_all.cfm) for help.

```python
<p align="center">
	Enjoy learning new knowledge. &#128536;
</p>
```

#### Example

<p align="center">
	Enjoy learning new knowledge. &#128536;
</p>

### Resolution 2 (recommended in main content)

Use the `:content:`  syntax; see [EmojiMart](https://missiveapp.com/open/emoji-mart).

```python
Enjoy learning new knowledge. :kissing_heart:
```

#### Example

Enjoy learning new knowledge. :kissing_heart:

**Note:** This method will not work in the HTML of the local Markdown editor like Typora. Notwithstanding, it **works** in GitHub Markdown. If you prefer to edit content locally and then push it to the remote repository, use UTF-8 encoding of Emoji, which makes the two happy.

#### Example

<p align="center">
	Enjoy learning new knowledge. :kissing_heart:
</p>
