# Passage
> A ***** made with ***** [Vue](https://github.com/vuejs/vue), [D3](https://github.com/d3/d3), and [Three.js](https://github.com/mrdoob/three.js/).

#### Try it out at *****[www.kaleidosync.com](https://www.kaleidosync.com)!

## Installation

Follow these steps to get the project up and running on your local machine.

### Prerequisites

Ensure the following software is installed on your machine:

- [Node.js and npm](https://nodejs.org/en/download/)
- [Git](https://git-scm.com/downloads)

### Setup

#### Step 1: Clone the Repository

In a directory of your choice, clone the repository using the following command:

```shell
git clone https://github.com/levgrishchuk/Passage.git
```

#### Step 2: Create Spotify Developer App

1. Go to [Spotify Developer Dashboard](https://developer.spotify.com/dashboard/applications) and log in.
2. Click on "Create an App", fill out the necessary information, and note your `client id` and `client secret`.
3. Add `http://localhost:3000/` (make sure to include the trailing "/") as a Redirect URI in the app settings.

#### Step 3: Setup MongoDB

Follow [MongoDB's official guide](https://docs.mongodb.com/manual/installation/) to create a new Atlas project, build a database, whitelist your IP, add a database user, and obtain the `connection URI`. If you prefer a video guide, [this tutorial](https://www.youtube.com/watch?v=KKyag6t98g8) can help you set it up.

#### Step 4: Create Environment Files

1. In the root directory, create a `.env` file and populate it like so:
    ```shell
    NODE_ENV = "development"
    client_id = "<your-client-id>"
    client_secret = "<your-client-secret>"
    redirect_uri = "http://localhost:3000/"
    mongoURI = "<your-mongoURI>"
    ```
2. In the `client` directory, create a `.env` file and populate it like so:
    ```shell
    NODE_ENV = "development"
    REACT_APP_client_id = "<your-client-id>"
    client_secret = "<your-client-secret>"
    REACT_APP_redirect_uri = "http://localhost:3000/"
    mongoURI = "<your-mongoURI>"
    ```
Replace `<your-client-id>`, `<your-client-secret>`, and `<your-mongoURI>` with the values you obtained in Steps 2 and 3. Remember to include quotation marks ("") around your values.

For the `<your-mongoURI>`, remember to replace PASSWORD with your MongoDB user password. Special characters like %, @, and others should be URL-encoded.

#### Step 5: Install Dependencies

From the root directory, run the following commands:

```shell
# Install root dependencies
npm install
# Change into the client directory
cd client
# Install client dependencies
npm install
# Navigate back to root
cd ..
```

#### Step 6: Run the Application

Finally, start the application with:

```shell
npm run dev
```

