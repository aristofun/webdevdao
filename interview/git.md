# Вопросы по git с собеседований

1. Что такое VCS? Что такое Git? Почему его используют?

    <details>
      <summary>Ответ</summary>
      Version Control System, для облегчения работы с изменяющейся информацией.

      https://ru.wikipedia.org/wiki/%D0%A1%D0%B8%D1%81%D1%82%D0%B5%D0%BC%D0%B0_%D1%83%D0%BF%D1%80%D0%B0%D0%B2%D0%BB%D0%B5%D0%BD%D0%B8%D1%8F_%D0%B2%D0%B5%D1%80%D1%81%D0%B8%D1%8F%D0%BC%D0%B8
    </details>

1. Как создать репозиторий и добавить в него проект?

    <details>
      <summary>Ответ</summary>

      * Создание на гитхабе
      * `git init` у себя
      * `git remote add origin (название репо)`
      * `git push -u origin master`
      * `git pull` (взять изменения проекта)
    </details>

1. Как загрузить удаленный репозиторий?

    <details>
      <summary>Ответ</summary>
      `git clone <адрес репозитория>`
    </details>

1. Что такое коммит? Как посмотреть историю коммитов?

    <details>
      <summary>Ответ</summary>
      Подтверждение изменений.

      `git log`
    </details>

1. Что такое ветка в Git?

    <details>
      <summary>Ответ</summary>
      Ответвление от основной ветки для работы с определенной фичей.
    </details>

1. Отличия между командами `merge` и `rebase`?

    <details>
      <summary>Ответ</summary>

      Отличие в качестве и красоте истории, при `rebase` коммит встает на первое место и история становится красивой.
    </details>

1. Как загрузить последние изменения с определенной ветки?

    <details>
      <summary>Ответ</summary>
      `git pull --rebase`
    </details>

1. Как отправить свои изменения на удаленный репозиторий?

    <details>
      <summary>Ответ</summary>

      * `git add .`
      * `git commit -m "Commit message"
      * `git push`
    </details>

1. Как добавить изменения в уже созданный коммит? изменить название такого коммита?

    <details>
      <summary>Ответ</summary>

      * `git add .`
      * `git commit --amend`
    </details>

1. Как удалить ветку локально и с удаленного репозитория?

    <details>
      <summary>Ответ</summary>

      * `git branch -d new-branch`
      * `git branch -d origin new-branch`
      * `git push origin :new-branch`
    </details>

1. Что такое запросы на слияние (pull requests)? Как их создавать?

    <details>
      <summary>Ответ</summary>
      https://www.youtube.com/watch?v=M7ZYkjOWr6g

      https://www.youtube.com/watch?v=Wz7RDh6CylI
    </details>

1. Как перенести изменени из одной ветку в другую (2 способа)?

    <details>
      <summary>Ответ</summary>
      Использовать cherry-pick

      https://www.youtube.com/watch?v=BP53rBf1PUE

      https://www.youtube.com/watch?v=-fDa6ntlBXg

      Второй способ немного сложнее, нужно сделать ответвление и затем смержить в обе ветки код.
    </details>

1. Разница между git и svn (если есть)?
1. Для чего нужен SSH ключ?

    <details>
      <summary>Ответ</summary>
      ssh ключи используются для облегчённой авторизации на различных сервисах.

      ssh ключ состоит из двух частей

      * id_rsa — закрытая часть, которая должна быть доступна только вам, ни кому и ни когда нельзя давать к ней доступ, этот файл можно переносить с компа на ком. так чтобы был у вас был только 1 ключ, но тут свои риски, например у вас в одном месте кто-то получил доступ к $HOME, следовательно все ваши акаунты потенциально взломали
      * id_rsa.pub — открытая часть, бесполезна без закрытой, её можно показывать всем, можно даже повесить на своём сайте, чтобы желающие дать вам доступ на свой сервер могли быстро добавить ваш открытый ключ в файл `~/.ssh/authorized_keys`.
    </details>

1. Git commit -am — в каких случаях необходимо писать -am вместе, а когда просто -a или -m?

Где искать ответы:

* https://git-scm.com/docs
* https://githowto.com/ru
* https://learn.javascript.ru/screencast/git
