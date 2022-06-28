# Entities
## PostgreSQL
### AuthService
## MongoDB
### ClientService
> Interaction with the MongoDB collection "Client" and CRUD for a client user.

```ts
let Client = {
    _id: double,
    globalUserId: double,
    firstName: string,
    lastName: string,
    phoneNumber: string,
    termsOfUse: boolean,
    locations: [{lat: float, lng: float, address: string, name: string}, ...],
    patronageCode: string,
    notification: boolean,
}
```

### RestaurantService
> Interaction with the MongoDB collection "Restaurant", "Menu", "Article" and CRUD for a restaurant user, menu, article.

```ts
let Restaurant = {
    _id: double,
    globalUserId: double,
    restaurantName: string,
    professional_mail: string,
    phoneNumber: string,
    termsOfUse: boolean,
    location: {lat: float, lng: float, address: string, name: string},
    patronageCode: string,
    notification: boolean,
    restaurantImage: ???,
}
```

```ts
let Menu = {
    _id: double,
    name: string,
    menuImage: ???,
    articles: [liste d'objets Article],
    price: number,
}
```

```ts
let Article = {
    _id: double,
    name: string,
    articleImage: ???,
    price: number,
}
```


### DeliverService
> Interaction with the MongoDB collection "Deliver" and CRUD for a deliver user.

```ts
let Deliver = {
    _id: double,
    globalUserId: double,
    firstName: string,
    lastName: string,
    phoneNumber: string,
    birthDate: dateTime,
    termsOfUse: boolean,
    location: {lat: float, lng: float, address: string, name: string},
    patronageCode: string,
    notification: boolean,
    movingRadius: number
}
```

### OrderService
> Interaction with the MongoDB collection "Order" for any user.

```ts
let Order = {
    _id: double,
    restaurant: Restaurant,
    client: Client,
    deliver: Deliver,
    status: Enum["à définir"],
    orderDatetime: Datetime,
    inOrder: [Article, Menu, ...],
    deliveryLocation: {lat: float, lng: float, address: string},
    clientComment: string,
    deliverComment: string,
    restaurantComment: string,
}
```
