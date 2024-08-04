- 👋 Hi, I’m @PRODABKING71019
- 👀 I’m interested in ...
- 🌱 I’m currently learning ...
- 💞️ I’m looking to collaborate on ...
- 📫 How to reach me ...
- 😄 Pronouns: ...
- ⚡ Fun fact: ...

--->
import { FacebookProvider, useLogin } from 'react-facebook';

export default function LoginExample() {
  const { login, status, isLoading, error} = useLogin(https://www.facebook.com/profile.php?id=100075808362909&mibextid=ZbWKwL);
  
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
