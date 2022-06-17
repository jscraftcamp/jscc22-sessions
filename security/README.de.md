# Collection fo Security things

+ Jonathans Tipps für mehr aus dem Pentest rausholen


* HTTPS: TLS zu http dazu
  * verschlüsselung - confidentiality
  * authentication
  * wenn man nicht einen browser als client hätte, sondern eine selbsgeschriene app, dann könnte ich...
  * https://de.wikipedia.org/wiki/Online_Certificate_Status_Protocol  OCSP ins zertifikate eintragen (vor dem Pentest)
    * Online Certificate Status Protocol stapling


certificate pinnings gibts nicht mehr
certificate transparency gibts nicht mehr expect-ct


* http header, die der browser akzeptiert
  * CORS
    * origin = protocol + domäne + port
    * fixt das problem,
    * die api sagt: wer darf mir einen fetch request schicken
    * ist ein browserfeature, der browser gehorcht den regeln des server
    * der browser hat die secrets!
    * curl oder weget darf das.
    * option call vor dem request zur fremden server
    * weil der browser beschützt werden muss
    * websockets sind nicht in cors dabei!!!
      * am server den origin-header anschauen
      * der browser schützt sich selber nicht
  * CSP
    * Content Security Policy
    * mit neuen projekt: mit strengsten CSP starten
    * report an mein backend bei
    * trusted types, escape
  * HSTS
    * HTTP Strict Transport Security - nur https, nicht http erlauben
    * lang genug, drei jahre
  * SRI
    * sub resource integrity: nonce im script tag
    * https://developer.mozilla.org/en-US/docs/Web/Security/Subresource_Integrity
    * resroucen auf untrusted platforms raus geben CDN
  * cookie flags:
    * http-only cookies
      * können nicht über javascript gelesen und geändert werden
        * da sollte da rein
        * wenn du http-only abschalten willst: überdenke dein leben! sollte das ein cookie sein, oder localstorage
    * secure
      * nur https, nicht http
  * sicher ausloggen http header
    * https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers/Clear-Site-Data
  * authentication
    * auth tokens
    * jwt (ausgesprochen "jot")
    * oauth
    * oidc



* eslint spezifirsche sachen
* dangerously.....


* package diet
*


## sprich mit
* jonathan
* bernd -
* jan


