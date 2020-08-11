# Cache Options en Wordpress

<h2><a id="user-content-base-de-datos-persistencia" class="anchor" aria-hidden="true" href="#base-de-datos-persistencia"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M7.775 3.275a.75.75 0 001.06 1.06l1.25-1.25a2 2 0 112.83 2.83l-2.5 2.5a2 2 0 01-2.83 0 .75.75 0 00-1.06 1.06 3.5 3.5 0 004.95 0l2.5-2.5a3.5 3.5 0 00-4.95-4.95l-1.25 1.25zm-4.69 9.64a2 2 0 010-2.83l2.5-2.5a2 2 0 012.83 0 .75.75 0 001.06-1.06 3.5 3.5 0 00-4.95 0l-2.5 2.5a3.5 3.5 0 004.95 4.95l1.25-1.25a.75.75 0 00-1.06-1.06l-1.25 1.25a2 2 0 01-2.83 0z"></path></svg></a>Base de datos (Persistencia)</h2>
<p>Hay varios metodos de almacenar información en wordpress con los plugin o en el uso general del wordpress.</p>
<h3><a id="user-content-options" class="anchor" aria-hidden="true" href="#options"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M7.775 3.275a.75.75 0 001.06 1.06l1.25-1.25a2 2 0 112.83 2.83l-2.5 2.5a2 2 0 01-2.83 0 .75.75 0 00-1.06 1.06 3.5 3.5 0 004.95 0l2.5-2.5a3.5 3.5 0 00-4.95-4.95l-1.25 1.25zm-4.69 9.64a2 2 0 010-2.83l2.5-2.5a2 2 0 012.83 0 .75.75 0 001.06-1.06 3.5 3.5 0 00-4.95 0l-2.5 2.5a3.5 3.5 0 004.95 4.95l1.25-1.25a.75.75 0 00-1.06-1.06l-1.25 1.25a2 2 0 01-2.83 0z"></path></svg></a>Options</h3>
<p>Las opciones son una funcionalidad para almacenar, cadenas, arreglos o objetos con el metodo clave valor.</p>
<ul>
<li>Nota: no se recomienda almacenar mas de 10 option, los ideal seria guardar un solo con un mismo nombre y recuperar la informacion, concatenar y volver a guardar.</li>
</ul>
<div class="highlight highlight-text-html-php"><pre><span class="pl-en">add_option</span>(<span class="pl-s1"><span class="pl-c1">$</span>name</span>, <span class="pl-s1"><span class="pl-c1">$</span>value</span>, <span class="pl-s1"><span class="pl-c1">$</span>deprecated</span>, <span class="pl-s1"><span class="pl-c1">$</span>autoload</span>);</pre></div>
<p>$name: Nombre o key de la opcion</p>
<p>$valie: Valor</p>
<p>$deprecated: NO se usa este parametro, pronto se eliminara, se le agrega null si se quiere usar el siguirente parametro.</p>
<p>$autoload: LLeva como valor [yes,no] y si es afirmativo la opcion sera cargada por <em>wp_load_alloptions</em>.</p>
<div class="highlight highlight-text-html-php"><pre><span class="pl-en">get_option</span>(<span class="pl-s1"><span class="pl-c1">$</span>option</span>);</pre></div>
<p>Como su nombre lo indica recupera la información de una opción.</p>
<div class="highlight highlight-text-html-php"><pre><span class="pl-en">update_option</span>(<span class="pl-s1"><span class="pl-c1">$</span>option_name</span>, <span class="pl-s1"><span class="pl-c1">$</span>newvalue</span>);</pre></div>
<p>Esta función se utiliza para actualizar oh crear una opción, wordpress la recomienda usar por encima de add_option.</p>
