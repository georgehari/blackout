În semn de protest față de reforma copyright-ului în UE, în forma actuală, care prevede filtre la upload și taxe pe link-uri, 
în 21 martie poți afișa o pagină neagră, cu un mesaj de protest în română și/sau engleză, în loc de site-ul tău propriu-zis.

Pachetul conține:
- pagina HTML cu textul în engleză
- pagina HTML cu textul în română
- pagina HTML cu textul bilingv
- un banner pătrat alb-negru.

Dacă vrei să redirecționezi întregul site spre această pagină neagră, adaugă acest cod în fișierul .htaccess și înlocuiește cu numele domeniului tău și al paginii de blackout:

RewriteEngine on

RewriteCond %{HTTP_HOST} ^domeniulmeu.com$ [OR]
RewriteCond %{HTTP_HOST} ^www.domeniulmeu.com$
RewriteRule ^/?$ "http://www.domeniulmeu.com/paginablackout.html" [R=301,L]
