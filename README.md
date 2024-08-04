- 👋 Hi, I’m @PRODABKING71019
- 👀 I’m interested in ...
- 🌱 I’m currently learning ...
- 💞️ I’m looking to collaborate on ...
- 📫 How to reach me ...
- 😄 Pronouns: ...
- ⚡ Fun fact: ...

<!---
PRODABKING71019/PRODABKING71019 is a ✨ special ✨ repository because its `README.md` (this file) appears on your GitHub profile.
You can click the Preview link to take a look at your changes.
--->
import { FacebookProvider, useLogin } from 'react-facebook';

export default function LoginExample() {
  const { login, status, isLoading, error} = useLogin();
  
  async function handleLogin() {
    try {
      const response = await login({
        scope: 'email',
      });

      console.log(response.status);
    } catch (error: any) {
      console.log(error.message);
    }
  }

  return (
    <button onClick={handleLogin} disabled={isLoading}>
      Login via Facebook
    </button>
  );
}
