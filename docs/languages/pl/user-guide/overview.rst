.. _user-guide.overview:

Pierwsze kroki z Zend Framework 2
=================================

Ten poradnik ma na celu dać wprowadzenie do korzystania z Zend Framework 2 , 
tworząc prostą aplikację z bazy danych za pomocą paradygmatu Model-View-Controller (Model-Widok-Kontroler). 
Na koniec będziesz mieć działając aplikację ZF2 i będziesz mógł grzebać w kodzie, aby dowiedzieć się więcej o tym, 
jak to wszystko działa.

.. _user-guide.overview.assumptions:

Kilka założeń
-------------

Ten poradnik zakłada, że używasz PHP w wersji co najmniej 5.3.3, Apache jako serwera WWW i MySQL,
dostępnego za pośrednictwem rozszerzenia PDO. Instalacja Apache musi mieć zainstalowane i skonfigurowane rozszerzenie 
mod_rewrite.

Należy również upewnić się, że Apache jest skonfigurowany do obsługi plików  ``.htaccess``. 
Jesli nie, należy wówczas zmienić ustawienia:

.. code-block:: apache
   :linenos:

    AllowOverride None

na

.. code-block:: apache
   :linenos:

    AllowOverride FileInfo
    
w pliku httpd.conf. Sprawdź szczegóły w dokumentacji twojej dystrybucji. Nie będziesz w stanie przejść 
do dowolnej strony w tym kursie, innej niż na strona główna, jeśli nie skonfigurujesz poprawnie mod_rewrite 
i obsługi plików ``htaccess``.

.. note::

Alternatywnie, jeśli używasz PHP 5.4+ można użyć zamiast Apache, wbudowanego serwera WWW.

Aplikacja przewodnika
---------------------

Aplikacja jaką zbudujemy, to  prosty system do wyświetlania spisu albumów które posiadamy.
Strona główna wyświetli naszą kolekcję i pozwoli nam dodawać, edytować i usuwać płyty. 
Będziemy potrzebować czterech stron w naszej witrynie:

+------------------+--------------------------------------------------------------+
| Strona           | Opis                                                         |
+==================+==============================================================+
| Lista albumów    | Wyświetli listę albumów i linki do ich edycji i usuwania.    |
|                  | Oprócz tego będzie zawierać link do dodania nowego albumu.   |
+------------------+--------------------------------------------------------------+
| Dodaj nowy album | Ta strona będzie zawierać formularz dodawania nowego albumu. |    
+------------------+--------------------------------------------------------------+
| Edytuj album     | Ta strona będzie zawierać formularz edycji albumu.           |
+------------------+--------------------------------------------------------------+
| Usuń album       | Ta strona wyświetli pytanie potwierdzające, czy chcemu       |
|                  | usunąć album, a następnie go usunie.                         |
+------------------+--------------------------------------------------------------+


