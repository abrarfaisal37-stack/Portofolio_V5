Portfolio V5
Hello everyone! 👋
I’m Abrar Ala, and I’m excited to share my Portfolio V5 website project that I’ve developed to showcase my work, achievements, and skills.
🚀 Live Demo
Website Link: https://www.abrar.my.id
🛠️ Tech Stack
This project uses modern web technologies:
ReactJS – Frontend framework
Tailwind CSS – Utility-first CSS framework
Supabase – Backend for portfolio data, certificates, and comments
AOS – Animate On Scroll library
Framer Motion – Animation library
Lucide – Icon library
Material UI – React component library
SweetAlert2 – Beautiful alert dialogs
📋 Prerequisites
Before running the project, ensure you have:
Node.js (v14.x or higher)
npm or yarn
🏃‍♂️ Getting Started
Clone the Repository
git clone https://github.com/AbrarAla/Portfolio_V5.git
cd Portfolio_V5
Install Dependencies
npm install
If you face peer dependency issues:
npm install --legacy-peer-deps
Run the Development Server
npm run dev
Open in Browser
Access the app via the URL shown in your terminal (usually http://localhost:5173).
🏗️ Building for Production
npm run build
The production-ready files will be in the dist folder. Upload this folder to your hosting server.
⚙️ Supabase Configuration
All backend data (portfolio projects, certificates, comments) is managed through Supabase.
Create a Supabase Project
Keep your Project URL and anon public key handy.
Setup Database Tables & Policies
Run the provided SQL scripts to create projects, certificates, portfolio_comments tables, RLS policies, and insert example data.
Enable Realtime (for Comments)
Go to Table Editor > portfolio_comments and enable Realtime.
🔧 Environment Variables
Create a .env file in the root:
VITE_SUPABASE_URL=your-supabase-url
VITE_SUPABASE_ANON_KEY=your-supabase-anon-key
All variables must start with VITE_ for Vite.
Restart your server after modifying .env.
Do not commit .env to version control.
Supabase Client Example (src/supabase.js)
import { createClient } from '@supabase/supabase-js'

const supabaseUrl = import.meta.env.VITE_SUPABASE_URL
const supabaseKey = import.meta.env.VITE_SUPABASE_ANON_KEY

if (!supabaseUrl || !supabaseKey) {
  throw new Error("Supabase URL and Anon Key are required. Check your .env file.")
}

export const supabase = createClient(supabaseUrl, supabaseKey)
🚨 Troubleshooting
Make sure Node.js is installed correctly.
Verify the project directory is correct.
Ensure dependencies are installed without errors.
Confirm your Supabase .env config is correct and server restarted.
Clear browser cache if needed.
📝 Usage & Credits
Feel free to use this project, but please give proper credit. Thank you! 🙏

## 📞 Contact

If you have any questions or need help with the setup, feel free to reach out\!


-----

⭐ If this project helped you, please consider giving it a star on GitHub\!
