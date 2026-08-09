# COMP1842 – Vocab Builder

A multilingual vocabulary management and learning app for **English – German – French**.

| Part        | Technology                              |
|-------------|-----------------------------------------|
| Frontend    | Vue.js 2, Vue Router, Semantic UI, Axios|
| Backend     | Node.js, Express 5, Mongoose            |
| Database    | MongoDB (local, port 27017)             |

---

| Requirement | Details                    |
|-------------|----------------------------|
| Node.js     | v16 or higher (recommended)|
| MongoDB     | Running on port 27017      |
| npm         | Comes with Node.js         |

Check if MongoDB is running:

bash
mongosh
 or
mongo
If MongoDB is not installed, install and start the service first.

**How to Run**

**Step 1 – Backend**
Bashcd server ,
npm install ,
node server.js.
On success you should see:
textConnected to MongoDB
Server is running at http://localhost:8000


**Step 2 – Frontend**
Open a new terminal:
Bashcd front-end, 
npm install, 
npm run serve .
Open the browser at the address shown by Vue CLI (usually http://localhost:8080).

**Important Notes**

Do not upload the node_modules folders.
Anyone who clones the project only needs to run npm install in each folder.
Backend connects to: mongodb://localhost:27017/vocab-builder
Frontend calls the API at: http://localhost:8000/vocabs

Before zipping or pushing to Git, remove node_modules if present:
Bashrm -rf server/node_modules
rm -rf front-end/node_modules

COMP1842-Vocab-Builder/
COMP1842-Vocab-Builder/
├── server/
│   ├── api/
│   │   ├── controllers/
│   │   │   └── vocabsController.js
│   │   ├── models/
│   │   │   └── vocabmodels.js
│   │   └── routes/
│   │       └── vocabs.js
│   ├── package.json
│   └── server.js
├── front-end/
│   ├── public/
│   │   ├── favicon.ico
│   │   └── index.html
│   ├── src/
│   │   ├── components/
│   │   │   ├── WordForm.vue
│   │   │   └── HelloWorld.vue
│   │   ├── views/
│   │   │   ├── Words.vue
│   │   │   ├── Add.vue
│   │   │   ├── Edit.vue
│   │   │   ├── Show.vue
│   │   │   ├── Test.vue
│   │   │   └── About.vue
│   │   ├── helpers/
│   │   │   └── helpers.js
│   │   ├── App.vue
│   │   ├── main.js
│   │   └── router.js
│   └── package.json
└── README.md


| Folder      | Purpose                              |
|-------------|--------------------------------------|
| `server/`   | Backend API (Express + MongoDB)      |
| `front-end/`| Frontend app (Vue.js)                |
| `api/`      | Controllers, Models, Routes          |
| `src/`      | Vue components, views, helpers       |


**Features**

| Page   | Path              | Description                                |
|--------|-------------------|--------------------------------------------|
| Words  | `/words`          | List all vocabulary entries                |
| New    | `/words/new`      | Add a new word (English / German / French) |
| Show   | `/words/:id`      | View details of a single word              |
| Edit   | `/words/:id/edit` | Edit a word                                |
| Test   | `/test`           | Vocabulary quiz / test                     |
| About  | `/about`          | Project information                        |


Backend API
Base URL: http://localhost:8000/vocabs


| Method | Endpoint  | Description         |
|--------|-----------|---------------------|
| GET    | `/`       | Get all words       |
| GET    | `/:id`    | Get one word by ID  |
| POST   | `/`       | Create a new word   |
| PUT    | `/:id`    | Update a word       |
| DELETE | `/:id`    | Delete a word       |

Each word has 3 required fields: english, german, french.


| Field    | Type   | Required | Description              |
|----------|--------|----------|--------------------------|
| english  | String | Yes      | English translation      |
| german   | String | Yes      | German translation       |
| french   | String | Yes      | French translation       |


| Service  | URL                              |
|----------|----------------------------------|
| Backend  | http://localhost:8000            |
| Frontend | http://localhost:8080            |
| API Base | http://localhost:8000/vocabs     |
| MongoDB  | mongodb://localhost:27017/vocab-builder |


































MethodEndpointDescriptionGET/Get all wordsGET/:idGet one word by IDPOST/Create a new wordPUT/:idUpdate a wordDELETE/:idDelete a word
Each word has 3 required fields: english, german, french.
