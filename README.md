# (Titlu)
LoopFader

## (Instalare)
Se utilizeaza doar MAX si o aplicatie OSC de pe telefon https://play.google.com/store/apps/details?id=com.ffsmultimedia.osccontroller

## (Utilizare)
Cu ajutorul mesajelor replace putem selecta orice fisiere audio pe care le avem pe dispozitivul nostru. Cu cele mesaje replace vom incarca 2 piese. Piesele vor fi incarcate cu ajutorul obiectului "buffer" ce incarca piesa intr-un buffer. Apoi cu ajutorul obiectului "info" vom afisa timpul total al piesei in milisecunde. Acesta valoare o vom imparti in cate slice-uri dorim. Eu am folosit 32 de slice-uri, dar valoarea se poate seta arbitrar. Astfel vom avea timpul in milisecunde pe care il va avea fiecare slice. Astfel, pentru primul slice incepem de la 0, pentru al doilea slice incepem de la 0 + duratia slice-ului, pentru al treilea slice incepem de la 0 + durata a doua slice-uri, si asa mai departe. Acest lucru este realizat cu ajutorul obiectului trigger, in care de fiecare data cand incarcam o valoare a slide ului de la 0 la 31, incarca valoarea respectiva si apoi da si un bang, pentru calcularea instanta a noului slice selectat. Calculul intervalului este {(durata unui slice * numarul slice-ului), ((durata unui slice * numarul slice-ului) + durata unui slice)}

## (Istoric)

(13.05) ...

(3.06) ...

(X.06) ...

## (Link-uri)
...

# Dezvoltarea proiectului

Pentru început:

1. Creează-ți cont pe Github
2. Download și install [Github Desktop](https://desktop.github.com/)
3. Citește [acest ghid](https://charlesmartin.com.au/blog/2020/08/09/student-project-repository) și ține la îndemână [Markdown Cheat Sheet](https://www.markdownguide.org/cheat-sheet).

Apoi, procesul este următorul (inspirat de [aici](https://cs.anu.edu.au/courses/comp1720/deliverables/05-major-project/#submission-process)):

1. *fork* al acestui template către propriul tău cont de Github

![](assets/fork.gif)

_(dacă preferi cumva ca repo-ul să nu fie vizibil de către public, îl poți seta ca Private din Settings - "Change visibility". Atunci trebuie să mă adaugi drept colaborator, ca eu să am acces.)_

2. *clone* al repo-ului din Github Desktop pentru a-l downloada local

![](assets/clone.gif)

3. *commit* și *push* pe măsură ce lucrezi la proiect. Ultima versiune push-ată pe server înainte de deadline va conta pentru evaluare.

![](assets/commit.gif)

## Elemente obligatorii

1. Acest readme completat. Titlu, descriere, mod de utilizare, istoric, link-uri utile.

   Poți include și imagini și chiar [gif-uri animate](https://www.screentogif.com/), sau link-uri către materiale audio/video.
   
   Vezi [aici](https://charlesmartin.com.au/blog/2020/08/09/student-project-repository) mai multe sugestii.

2. [Declarația de originalitate](statement-of-originality.yml) completată. Tot ce nu este inclus acolo va fi considerat 100% contribuție proprie.

    *(formatul este adaptat de [aici](https://gitlab.cecs.anu.edu.au/comp1720/2018/comp1720-2018-major-project/-/blob/master/statement-of-originality.yml). Da, este un pic ironic să refolosim un doc [de altundeva](https://cs.anu.edu.au/courses/comp1720/resources/faq/#how-do-i-fill-out-my-statement-of-originality), dar menționăm sursa deci nu este plagiat!)*

3. Proiectul în sine. Tot codul trebuie să fie prezent, proiectul trebuie să poată rula conform instrucțiunilor din readme. Dacă e nevoie de asset-uri mari (sunete, video etc), [folosește Git LFS](https://git-lfs.github.com/) sau include link de download în instrucțiunile de instalare.

