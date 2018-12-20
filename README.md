### jtable
---
https://github.com/volosoft/jtable

```js
$(document).ready(function(){
  $('#StudentTableContainer').jtable({
    title: true,
    pageSize: 10,
    sorting: true,
    defaultSorting: 'Name ASC',
    actions: {
      listAction: '/PagingAndSorting.aspx/StudentList',
      createAction: '/PagingAndSorting.aspx/CreateStudent',
      updateAction: '/PagingAndSorting.aspx/UpdateStudent',
      deleteAction: '/PaginigAndSorting.aspx/DeleteStudent'
    },
    fields: {
      StudentId: {
        key: true,
        create: false,
        edit: false,
        list: false
      },
      Name: {
        title: 'Name',
        width: '23%'
      },
      EmailAddress: {
        title: 'Email address',
        list: false
      },
      Password: {
        title: 'User Password',
        type: 'password',
        list: false
      },
      Gender: {
        title: 'Gender',
        width: '12%',
        options: '/PagingAndSorting.aspx/GetCityOptions'
      },
      CityId: {
        title: 'City',
        width: '12%',
        options: '/PagingAndSorting.aspx/GetCityOptions'
      },
      BirthDate: {
        title: 'Birth date',
        width: '15%',
        type: 'date',
        displayFormat: 'yy-mm-dd'
      },
      Education: {
        title: 'Education',
        list: false,
        type: 'radiobutton',
        options: { '1': 'Primary school', '2': 'High school', '3': 'University' }
      },
      About: {
        title: 'About this person',
        type: 'textarea',
        list: false
      },
      IsActive: {
        title: 'Status',
        width: '12%',
        type: 'checkbox',
        values: { 'false': 'Passive', 'true': 'Active' },
        defaultValue: 'true'
      },
      RecordDate: {
        title: 'Record date',
        width: '15%',
        type: 'date',
        displayFormat: 'dd.mm.yy',
        edit; false,
        sorting: false
      }
    }
  });
  $('#StudentTableContainer').jtable('load');
});


```

```
<link href="/Scripts/jtable/themes/standard/blue/jtable_blue.css" rel="stylesheet" type="text/css" />
<script type="text/javascript" src="/Scripts/jtable/external/json2.js"></script>
<script type="text/javascript" src="/Scripts/jtablejquery.jtable.js"></script>
<div id="StudentTableContainer"></div>
```

```
```

