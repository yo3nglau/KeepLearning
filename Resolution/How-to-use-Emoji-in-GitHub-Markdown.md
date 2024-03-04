## Resolution: How to use Emoji in GitHub Markdown

### Resolution 1 (especially work in HTML)

Represent specific Emoji with decimal (or hexadecimal) encoding; see [here](https://www.w3schools.com/charsets/ref_emoji_smileys.asp) or [here](https://www.quackit.com/character_sets/emoji/emoji_v3.0/unicode_emoji_v3.0_characters_all.cfm) for help.

```python
<p align="center">
	Enjoy learning new knowledge. &#128536;
</p>
```

#### Example

<p align="center">
	Enjoy learning new knowledge. &#128536;
</p>

### Resolution 2

Use the `:content:`  syntax; see [EmojiMart](https://missiveapp.com/open/emoji-mart).

```python
Enjoy learning new knowledge. :kissing_heart:
```

#### Example

Enjoy learning new knowledge. :kissing_heart:

**Note: **This kind of method will not work in HTML.

#### Failure

<p align="center">
	Enjoy learning new knowledge. :kissing_heart:
</p>

