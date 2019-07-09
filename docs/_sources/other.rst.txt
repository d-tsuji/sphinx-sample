その他の機能
==================================

---------------------------------
テーブル
---------------------------------

=====  =====  =======
A      B      A and B
=====  =====  =======
False  False  False
True   False  False
False  True   False
True   True   True
=====  =====  =======

---------------------------------
脚注
---------------------------------

これは 脚注 [#]_ です。

.. [#] 本文の下の方につける注記

---------------------------------
数式
---------------------------------

数式を有効にするには、``conf.py`` に ``sphinx.ext.mathjax`` という拡張モジュールを追加する必要があります。以下のような感じです。モジュールを有効にすれば、LaTeX で数式を記述することができます。

.. code-block:: none
    :caption: conf.py

    # Add any Sphinx extension module names here, as strings. They can be
    # extensions coming with Sphinx (named 'sphinx.ext.*') or your custom
    # ones.
    extensions = ['sphinx.ext.mathjax'
    ]
    
`N` 個の整数 :math:`d[0], d[1], \dots, d[N-1]` が与えられます。これは数式のサンプルです。

---------------------------------
TODO
---------------------------------

TODOも拡張モジュール ``sphinx.ext.todo`` を有効にすると記述できるようになります。あとでやりたいことを残しておくときに便利ですね。

.. code-block:: none
    :caption: conf.py

    # Add any Sphinx extension module names here, as strings. They can be
    # extensions coming with Sphinx (named 'sphinx.ext.*') or your custom
    # ones.
    extensions = ['sphinx.ext.mathjax', 'sphinx.ext.todo'
    ]
    
    [extensions]
    todo_include_todos = True

.. todo::

    これは TODO なので、後ほど調査する

TODOを表示する場所も選ぶことができます。今回は index ページに記載しておきましょう。表示させたい場所に ``` .. todolist:: ``` と記述しておけばよいです。

.. code-block:: rest

    .. sample-project documentation master file, created by
    sphinx-quickstart on Mon Jul  8 22:38:47 2019.
    You can adapt this file completely to your liking, but it should at least
    contain the root `toctree` directive.

    Welcome to sample-project's documentation!
    ==========================================

    .. toctree::
    :maxdepth: 2
    :caption: Contents:
    
    hello
    hierarchy
    code
    other

    Indices and tables
    ==================

    * :ref:`genindex`
    * :ref:`modindex`
    * :ref:`search`