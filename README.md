# Splitr

**Splitr** is a collaborative expense tracking and group management application built with Next.js, React, and Clerk authentication. It allows you to easily manage your contacts, create groups, and track shared expenses.

**Live Demo:** [splitr-red.vercel.app](https://splitr-red.vercel.app)



## ✨ Features

- **Authentication:** Secure sign-up and sign-in via [Clerk](https://clerk.com/) (see `/app/(auth)`).
- **Contacts Management:** View all your contacts; contacts are automatically added when you record expenses with someone.
- **Group Creation:** Create new groups, invite members, and manage group details through a user-friendly modal interface.
- **Expense Tracking:** (Presumed from structure; add more details if available).
- **Modern UI:** Responsive and accessible design using TailwindCSS and Headless UI components.
- **Real-time Data:** Integrates with Convex for live-updating data (see usage of `useConvexQuery` and `useConvexMutation`).
- **Notifications:** User feedback via toast notifications for actions like group creation.


## 🚀 Getting Started

### Prerequisites

- Node.js (v16+)
- Yarn or npm
- [Clerk](https://clerk.com/) account for authentication
- [Convex](https://convex.dev/) account/project for backend data

### Installation

1. **Clone the repository:**
   bash
   git clone https://github.com/sandeep0394/splitr.git
   cd splitr
   

2. **Install dependencies:**
   bash
   npm install
   # or
   yarn install
   

3. **Configure environment variables:**

   Copy `.env.example` to `.env.local` and add your Clerk and Convex credentials.

   
   # Example (add actual keys)
   NEXT_PUBLIC_CLERK_PUBLISHABLE_KEY=your-clerk-key
   CONVEX_URL=your-convex-url
   

4. **Run the development server:**
   bash
   npm run dev
   # or
   yarn dev
   
5. To run backend sever
   npx convex dev

6. Access the app at [http://localhost:3000](http://localhost:3000).

7. Actually to install few requirements the react version does not allow so you need to give 1 space and type --legacy-peer-deps

## 🗂️ Project Structure


app/
  (auth)/         # Authentication pages (sign-in, sign-up, layout)
  (main)/contacts # Contacts & groups UI and logic
    _components/  # Reusable contact/group components
  ...
components/       # Shared UI components (Button, Avatar, Dialog, etc.)
convex/           # Convex API definitions
hooks/            # Custom React hooks (e.g., useConvexQuery)
public/           # Static assets
styles/           # Global styles


## 💡 Usage Highlights

### Authentication

- All auth pages are in `/app/(auth)/`.
- Uses Clerk for secure, out-of-the-box authentication.

### Contacts & Groups

- View contacts and groups on `/contacts`.
- Create a new group via a modal (`CreateGroupModal`), search users, and invite them.
- Each contact/group links to a detailed page (see routing like `/person/[id]` or `/groups/[id]`).

### UI/UX

- Responsive layouts using Tailwind CSS utility classes.
- Dialogs, popovers, and input components for modern UX.

## 🛠️ Technologies Used

- **Frontend:** React, Next.js 13 (App Router), Tailwind CSS
- **Authentication:** Clerk
- **Backend/Realtime:** Convex
- **UI Components:** Custom & Headless UI
- **Notifications:** [sonner](https://sonner.emilkowal.ski/) for toasts
- **Iconography:** Lucide



## 📦 Deployment

Splitr is deployed on [Vercel](https://vercel.com/).

To deploy your own instance:
1. Push your repo to GitHub.
2. Connect your repo on Vercel.
3. Set environment variables for Clerk and Convex in the Vercel dashboard.
4. Deploy!

## 🙌 Contributing

Contributions are welcome!  
Feel free to open issues or submit pull requests.


## 👤 Author

- [sandeep0394](https://github.com/sandeep0394)

---

## 📣 Acknowledgements

- [Clerk](https://clerk.com/) for authentication
- [Convex](https://convex.dev/) for backend
- [Vercel](https://vercel.com/) for deployment
