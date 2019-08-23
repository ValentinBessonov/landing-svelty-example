<script>
  var contacts = {
    contacts: [
      {
        address: "г. Калуга ул. Кирова 78",
        formattingNumber: "8-4842-59-78-78",
        number: "84842597878"
      },
      {
        address: "г. Калуга ул. Кирова 7/47",
        formattingNumber: "8-920-615-11-17",
        number: "89206151117"
      },
      {
        address: "г. Обнинск ул. Аксенова 18",
        formattingNumber: "8-920-880-88-00",
        number: "89208808800"
      }
    ],
    groups: [
      {
        desc: "Группа в одноклассниках",
        url: "https://ok.ru/group/51814002196625"
      }
    ]
  };
</script>

<style>

</style>

<section id="contacts">
  <h1>Наши контакты</h1>
  <ul>
    {#each contacts.contacts as contact}
      <li>
        Адрес: {contact.address}
        <br />
        Телефон:
        <a href="tel:{contact.number}">{contact.formattingNumber}</a>
      </li>
      <hr>
    {/each}
  </ul>

  <h1>Соцсети</h1>
  {#each contacts.groups as group}
    <p>
      {group.desc}:
      <a href={group.url} target="_blank">{group.url}</a>
    </p>
  {/each}

</section>
