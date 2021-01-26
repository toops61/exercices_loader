# Produce maintainable CSS stylesheets with SASS

1 Base.

2 Utils.

3 Layout (mise en page).

4 Composants.

5 Pages.

6 Themes.

7 Vendors (tiers).

le directory base/ contient les fichiers qui définissent les fondations de votre site, par exemple la police de caractères et les normes que vous voulez appliquer sur tout votre site, telles que le box-sizing ;

dans utils/, vous rangez vos variables, fonctions, mixins et les  %placeholders pour les extensions (si vous en utilisez) ;

layouts/ est le dossier où vous mettez vos blocs BEM qui contiennent ce qui est réutilisable, par exemple un header pour les mises en page de grande taille ou un footer ;

components/ est utilisé pour ranger les blocs BEM qui sont plus indépendants, comme les boutons.

Alors que les layouts peuvent utiliser d’autres composants pour générer leurs contenus, les composants, eux, sont plus élémentaires. Par exemple, un formulaire doit être considéré comme un layout : la mise en page est une fonction vitale du bloc et il utilise d’autres blocs pour fonctionner,  comme des boutons. En revanche, le bouton lui-même est un composant car il n’a besoin d’aucun autre composant pour remplir sa fonction ;

pages/ contient les blocs de code qui ne s’appliquent qu’à une seule page. Vous utilisez des boutons dans tout votre site, en revanche votre page d’accueil comporte une section Citation et une grille de projets qui ne sont employés nulle part ailleurs. En d’autres termes, pages/ contient des règles spécifiques à une seule page qui ne seront pas réutilisées ailleurs ;

themes/, c’est ici que vous stockez le code thématique, par exemple un style customisé pour Noël ou pour l’été. On ne l’utilisera pas dans notre site ;

vendors/ est un directory pour des feuilles de style externes comme Bootstrap ou jQuery UI. En gros, il s’utilise pour tout CSS venant de l’extérieur. Utiliser des frameworks comme Bootstrap permet d’accélérer le développement d’un site, car ils contiennent des feuilles de style prédéfinies pour des choses comme les formulaires ou des boutons.

http://smacss.com/book/categorizing

Base
Layout
Module
State
Theme

Base rules are the defaults. They are almost exclusively single element selectors but it could include attribute selectors, pseudo-class selectors, child selectors or sibling selectors. Essentially, a base style says that wherever this element is on the page, it should look like this.

Examples of Base Styles

html, body, form { margin: 0; padding: 0; }
input[type=text] { border: 1px solid #999; }
a { color: #039; }
a:hover { color: #03C; }
Layout rules divide the page into sections. Layouts hold one or more modules together.

Modules are the reusable, modular parts of our design. They are the callouts, the sidebar sections, the product lists and so on.

State rules are ways to describe how our modules or layouts will look when in a particular state. Is it hidden or expanded? Is it active or inactive? They are about describing how a module or layout looks on screens that are smaller or bigger. They are also about describing how a module might look in different views like the home page or the inside page.

Finally, Theme rules are similar to state rules in that they describe how modules or layouts might look. Most sites don’t require a layer of theming but it is good to be aware of it.