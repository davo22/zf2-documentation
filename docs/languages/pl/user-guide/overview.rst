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
