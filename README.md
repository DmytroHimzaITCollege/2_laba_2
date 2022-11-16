# Звіт до роботи №3
## Тема: _Перша програма на ООП_
### Мета роботи: _Перша програма на ООП_
---
### Виконання роботи

- Результати виконання завдання *N1*;
Запустив даний код:
   ```python
      class MyName:
      """Опис класу / Документація
      """
      total_names = 0 #Class Variable

      def __init__(self, name=None) -> None:
         self.name = name if name is not None else self.anonymous_user().name #Class attributes / Instance variables
         MyName.total_names += 1 #modify class variable
         self.my_id = self.total_names

      @property
      def whoami(self): 
         """Class property
         return: повертаємо імя 
         """
         return f"My name is {self.name}"
      
      @property
      def my_email(self) -> str:
         """Class property
         return: повертаємо емейл
         """
         return self.create_email()
      
      def create_email(self) -> str:
         """Instance method
         """
         return f"{self.name}@itcollege.lviv.ua"

      @classmethod
      def anonymous_user(cls):
         """Classs method
         """
         return cls("Anonymous")
      
      @staticmethod
      def say_hello(message="Hello to everyone!"):
         """Static method
         """
         return f"You say: {message}"


   print("Let's Start!")

   names = ("Bohdan", "Marta", None)
   all_names = {name: MyName(name) for name in names}

   for name, me in all_names.items():
      print(f"""{">*<"*20}
   This is object: {me} 
   This is object attribute: {me.name} / {me.my_id}
   This is {type(MyName.whoami)}: {me.whoami} / {me.my_email}
   This is {type(me.create_email)} call: {me.create_email()}
   This is static {type(MyName.say_hello)} with defaults: {me.say_hello()} 
   This is class variable {type(MyName.total_names)}: from class {MyName.total_names} / from object {me.total_names}
   {"<*>"*20}""")

   print(f"We are done. We create {me.total_names} names! ??? Why {MyName.total_names}?")
   ```
Результат коду в терміналі:
   ```
   Let's Start!
   >*<>*<>*<>*<>*<>*<>*<>*<>*<>*<>*<>*<>*<>*<>*<>*<>*<>*<>*<>*<
   This is object: <__main__.MyName object at 0x000001C719CF4BD0> 
   This is object attribute: Bohdan / 1
   This is <class 'property'>: My name is Bohdan / Bohdan@itcollege.lviv.ua
   This is <class 'method'> call: Bohdan@itcollege.lviv.ua
   This is static <class 'function'> with defaults: You say: Hello to everyone! 
   This is class variable <class 'int'>: from class 4 / from object 4
   <*><*><*><*><*><*><*><*><*><*><*><*><*><*><*><*><*><*><*><*>
   >*<>*<>*<>*<>*<>*<>*<>*<>*<>*<>*<>*<>*<>*<>*<>*<>*<>*<>*<>*<
   This is object: <__main__.MyName object at 0x000001C719CF4B10> 
   This is object attribute: Marta / 2
   This is <class 'property'>: My name is Marta / Marta@itcollege.lviv.ua
   This is <class 'method'> call: Marta@itcollege.lviv.ua
   This is static <class 'function'> with defaults: You say: Hello to everyone! 
   This is class variable <class 'int'>: from class 4 / from object 4
   <*><*><*><*><*><*><*><*><*><*><*><*><*><*><*><*><*><*><*><*>
   >*<>*<>*<>*<>*<>*<>*<>*<>*<>*<>*<>*<>*<>*<>*<>*<>*<>*<>*<>*<
   This is object: <__main__.MyName object at 0x000001C71A0500D0> 
   This is object attribute: Anonymous / 4
   This is <class 'property'>: My name is Anonymous / Anonymous@itcollege.lviv.ua
   This is <class 'method'> call: Anonymous@itcollege.lviv.ua
   This is static <class 'function'> with defaults: You say: Hello to everyone! 
   This is class variable <class 'int'>: from class 4 / from object 4
   <*><*><*><*><*><*><*><*><*><*><*><*><*><*><*><*><*><*><*><*>
   We are done. We create 4 names! ??? Why 4?
   ```

- результати виконання завдання *N3*;
Модифікував програму додавши своє імя в список (Показав частину коду, та те що вона вивела)
   ```Python
   names = ("Bohdan", "Marta", "Dmytro", None)
   ```
Результат коду:
```
   This is object: <__main__.MyName object at 0x000001C719DCC350> 
   This is object attribute: Dmytro / 3
   This is <class 'property'>: My name is Dmytro / Dmytro@itcollege.lviv.ua
   This is <class 'method'> call: Dmytro@itcollege.lviv.ua
   This is static <class 'function'> with defaults: You say: Hello to everyone! 
   This is class variable <class 'int'>: from class 5 / from object 5
```

-  завдання *N2* ознайомтесь з кодом та зрозумійте за що відповідає кожен з рядків;

+ Виконав індивідуальні завдання для кождного пункту.
### Висновок: 
> у висновку потрібно відповісти на запитання:
- :question: Що зроблено в роботі - Подивився, що вивів скопійований код та дописав своє ім'я.;
- :question: Чи досягнуто мети роботи - Так, досягнуто;
- :question: Які нові знання отримано - вивчив більше основ Python;
- :question: Чи вдалось відповісти на всі питання задані в ході роботи - Ні.;
- :question: Чи вдалося виконати всі завдання - Ні.;
- :question: Чи виникли складності у виконанні завдання - Так.;
- :question: Чи подобається такий формат здачі роботи (Feedback)- Так.;
- :question: Побажання для покращення (Suggestions) - Немає побажань;
---# -
