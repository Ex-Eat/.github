# Entities
## PostgreSQL
### AuthService
## MongoDB
### ClientService
> Interaction with the MongoDB collection "Client" and CRUD for a client user.

```ts
let Client = {
    client_user_id: double,
    firstName: string,
    lastName: string,
    phoneNumber: string,
    birthDate: dateTime,
    termsOfUse: boolean,
    locations: [{lat: float, lng: float, adress: string, name: string}, ...],
    patronageCode: string,
    notification: boolean,
}
```

### RestaurantService
> Interaction with the MongoDB collection "Restaurant", "Menu", "Article" and CRUD for a restaurant user, menu, article.

```ts
let Restaurant = {
    restaurant_user_id: double,
    restaurant_name: string,
    professional_mail: string,
    phoneNumber: string,
    termsOfUse: boolean,
    location: {lat: float, lng: float, adress: string, name: string},
    patronageCode: string,
    notification: boolean,
    restaurant_image: ???,
}
```

```ts
let Menu = {
    menu_id: double,
    name: string,
    menu_image: ???,
    articles: [liste d'objets Article],
    price: number,
}
```

```ts
let Article = {
    article_id: double,
    name: string,
    article_image: ???,
    price: number,
}
```


### DeliverService
> Interaction with the MongoDB collection "Deliver" and CRUD for a deliver user.

```ts
let Deliver = {
    deliver_user_id: double,
    firstName: string,
    lastName: string,
    phoneNumber: string,
    birthDate: dateTime,
    termsOfUse: boolean,
    location: {lat: float, lng: float, adress: string, name: string},
    patronageCode: string,
    notification: boolean,
    moving_radius: number
}
```

### OrderService
> Interaction with the MongoDB collection "Order" for any user.

```ts
let Order = {
    order_id: double,
    restaurant: Restaurant,
    client: Client,
    deliver: Deliver,
    status: Enum["à définir"],
    order_datetime: Datetime,
    in_order: [Article, Menu, ...],
    delivery_location: {lat: float, lng: float, adress: string},
    client_comment: string,
    deliver_comment: string,
    restaurant_comment: string,
}
```
