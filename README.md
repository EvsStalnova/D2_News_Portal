# **Итоговое задание 2.9 (HW-03)**

##**_Проект News Portal**_

1. Модель Author
Модель, содержащая объекты всех авторов.
Имеет следующие поля:
- cвязь «один к одному» с встроенной моделью пользователей User;
- рейтинг пользователя. Ниже будет дано описание того, как этот рейтинг можно посчитать.
2. Модель Category
Категории новостей/статей — темы, которые они отражают (спорт, политика, образование и т. д.). Имеет единственное поле: название категории. Поле должно быть уникальным (в определении поля необходимо написать параметр unique = True).
3. Модель Post
Эта модель должна содержать в себе статьи и новости, которые создают пользователи. Каждый объект может иметь одну или несколько категорий.
Соответственно, модель должна включать следующие поля:
- связь «один ко многим» с моделью Author;
- поле с выбором — «статья» или «новость»;
- автоматически добавляемая дата и время создания;
- связь «многие ко многим» с моделью Category (с дополнительной моделью PostCategory);
- заголовок статьи/новости;
- текст статьи/новости;
- рейтинг статьи/новости.
  
4. Модель PostCategory
Промежуточная модель для связи «многие ко многим»:
- связь «один ко многим» с моделью Post;
- связь «один ко многим» с моделью Category.

5. Модель Comment
Под каждой новостью/статьёй можно оставлять комментарии, поэтому необходимо организовать их способ хранения тоже.
Модель будет иметь следующие поля:
- связь «один ко многим» с моделью Post;
- связь «один ко многим» со встроенной моделью User (комментарии может оставить любой пользователь, необязательно автор);
- текст комментария;
- дата и время создания комментария;
- рейтинг комментария.
