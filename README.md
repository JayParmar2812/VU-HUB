- Next.js Twitch Clone with Clerk Webhooks and Prisma
- This project is a Twitch clone built using Next.js, Clerk for authentication, and Prisma as the ORM to handle database interactions. The application aims to replicate the core 
  features of Twitch, such as user authentication, live streaming, chat functionality, and user profiles.

- Features
  User Authentication:

- Clerk Integration: Clerk provides a seamless authentication experience with features such as user registration, login, password reset, and social login options.

- Webhooks: Clerk webhooks are used to handle events such as user creation, updates, and deletions. These webhooks ensure that the application stays in sync with the Clerk user database.

- Database Management:

- Prisma ORM: Prisma is used to interact with the database. It provides a type-safe query builder and supports various databases like PostgreSQL, MySQL, and SQLite.

- Schema Definition: Prisma schema defines the database models for users, streams, chat messages, and other necessary entities.
- Live Streaming:

- Users can start live streams, which other users can view in real-time.
- Stream metadata, such as title and category, can be set and updated by the streamer.
- Chat Functionality:
 
- Real-time chat is implemented using WebSockets, allowing viewers to interact with streamers and other viewers.
- Chat messages are stored in the database, enabling chat history for each stream.
- User Profiles:

- Each user has a profile page displaying their information, past streams, and other relevant data.
- Users can follow other streamers to get notified when they go live.
- Technical Stack
- Next.js: A React framework that enables server-side rendering and static site generation. It provides a robust structure for building the front-end and back-end of the application.
- Clerk: Manages user authentication and provides webhooks for real-time updates on user-related events.
- Prisma: An ORM that simplifies database interactions and ensures type safety in queries.  
- WebSockets: Enables real-time communication for chat functionality.
- 📡 Streaming using RTMP / WHIP protocols
- 🌐 Generating ingress
- 🔗 Connecting Next.js app to OBS / Your favorite streaming software
- 🔐 Authentication
- 📸 Thumbnail upload
- 👀 Live viewer count
- 🚦 Live statuses
- 💬 Real-time chat using sockets
- 🎨 Unique color for each viewer in chat
- 👥 Following system
- 🚫 Blocking system
- 👢 Kicking participants from a stream in real-time
- 🎛️ Streamer / Creator Dashboard
- 🐢 Slow chat mode
- 🔒 Followers only chat mode
- 📴 Enable / Disable chat
- 🔽 Collapsible layout (hide sidebars, chat etc, theatre mode etc.)
- 📚 Sidebar following & recommendations tab
- 🏠 Home page recommending streams, sorted by live first
- 🔍 Search results page with a different layout
- 🔄 Syncing user information to our DB using Webhooks
- 📡 Syncing live status information to our DB using Webhooks
- 🤝 Community tab
- 🎨 Beautiful design
- ⚡ Blazing fast application
- 📄 SSR (Server-Side Rendering)
- 🗺️ Grouped routes & layouts
- 🗃️ MySQL
- 🚀 Deployment

### Prerequisites

**Node version 18.17 or later**

### Install packages

```shell
npm i
```

### Setup .env file

```js
NEXT_PUBLIC_CLERK_PUBLISHABLE_KEY=
CLERK_SECRET_KEY=
NEXT_PUBLIC_CLERK_SIGN_IN_URL=/sign-in
NEXT_PUBLIC_CLERK_SIGN_UP_URL=/sign-up
NEXT_PUBLIC_CLERK_AFTER_SIGN_IN_URL=/
NEXT_PUBLIC_CLERK_AFTER_SIGN_UP_URL=/
CLERK_WEBHOOK_SECRET=

DATABASE_URL=

LIVEKIT_API_URL=
LIVEKIT_API_KEY=
LIVEKIT_API_SECRET=
NEXT_PUBLIC_LIVEKIT_WS_URL=

UPLOADTHING_SECRET=
UPLOADTHING_APP_ID=
```

### Setup Prisma

Add MySQL Database (I used PlanetScale)

````shell
npx prisma generate
npx prisma db push

`

### Start the app

```shell
npm run dev
````
