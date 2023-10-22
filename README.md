# HomeWork_6




    **Правила оформления README.md **

</GITHUB>

***

Превый абзац

---

Второй абзац


# Заголовок 1-го уровня
## Заголовок 2-го уровня
### Заголовок 3-го уровня 

...

###### Заголовок 6-го уровня


Оформление ссылки [Django GitHub](https://github.com/django/django)

<https://github.com/django/django>


**Выделение жирным шрифтом**
***Выделение наклонным жирным шрифтом***

`Выделенные слова`

    Выделение блок
    текста
    dir/fonts


Блок теста с подсветкой синтаксиса кода указываем тройной апостраф и после него указываем язык синтаксиса подсветки

```python
print('hello world')
```

> Текст
>
> Продолжение текста в выделенном блоке

 Нумерованный список

* Пункт 1
* Пункт 2
* Пункт 3

 Нумерованный список 

1. Пункт 1
2. Пункт 2
3. Пункт 3

_Наклонный _ _шрифт_

![pic_of_nature](https://w.forfun.com/fetch/15/1529e2e309c041538dc8a789e69b7e60.jpeg)





from string import ascii_uppercase

class Alphabet:
    def __init__(self, lang, letters_str):
        self.lang = lang
        self.letters = list(letters_str)


    def print(self):
        print(self.letters)

    def letters_num(self):
        print(len(self.letters))



class EngAlphabet(Alphabet):

    __letters_num = 26


    def __init__(self):
        super().__init__('En', ascii_uppercase )

    def  is_en_letter(self, letter):
        if letter.upper() in self.letters:
            return True
        return False
    
    def letters_num(self):
        return EngAlphabet.__letters_num
    
    @staticmethod
    def example():
        print('Eng Example: This is example.')


if __name__ == '__main__':
    eng_alphabet = EngAlphabet()
    eng_alphabet.print()
    print(eng_alphabet.letters_num())
    print(eng_alphabet.is_en_letter('F'))
    print(eng_alphabet.is_en_letter('f'))
    print(eng_alphabet.is_en_letter('Щ'))
    print(eng_alphabet.is_en_letter('щ'))
    EngAlphabet.example()
