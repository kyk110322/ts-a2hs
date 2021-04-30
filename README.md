# ts-a2hs

working on a2hs on ts.

npx create-react-app my-app --template cra-template-pwa-typescript

change 
serviceWorkerRegistration.unregister(); -> serviceWorkerRegistration.register();
on index.tsx

if you want pop up on mobile.

on public folder
index.html

add


     <script>
      window.addEventListener('load', () => {
        if ('serviceWorker' in navigator) {
          navigator.serviceWorker
            .register('sw.js')
            .then(registration => console.log('registered', registration))
            .catch(error => console.log('error', error));
        }
      });
    </script>
    
    create sw.js
    
    
    self.addEventListener('fetch', function (event) {});
