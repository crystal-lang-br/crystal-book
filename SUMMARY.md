# Sumário

* [Introdução](README.md)
* [Instalação](installation/README.md)
   * [No Debian e Ubuntu](installation/on_debian_and_ubuntu.md)
   * [No RedHat e CentOS](installation/on_redhat_and_centos.md)
   * [No Arch Linux](installation/on_arch_linux.md)
   * [No Mac OSX usando Homebrew](installation/on_mac_osx_using_homebrew.md)
   * [De um tar.gz](installation/from_a_targz.md)
   * [Do código-fonte](installation/from_source_repository.md)
* [Usando o compilador](using_the_compiler/README.md)
* [Visão-Geral e Exemplos](overview/README.md)
   * [Olá Mundo!](overview/hello_world.md)
   * [Servidor HTTP](overview/http_server.md)
* [Sintaxe e semântica](syntax_and_semantics/README.md)
   * [Comentários](syntax_and_semantics/comments.md)
   * [Literais](syntax_and_semantics/literals.md)
       * [Nil](syntax_and_semantics/literals/nil.md)
       * [Bool](syntax_and_semantics/literals/bool.md)
       * [Integers](syntax_and_semantics/literals/integers.md)
       * [Floats](syntax_and_semantics/literals/floats.md)
       * [Char](syntax_and_semantics/literals/char.md)
       * [String](syntax_and_semantics/literals/string.md)
       * [Symbol](syntax_and_semantics/literals/symbol.md)
       * [Array](syntax_and_semantics/literals/array.md)
       * [Hash](syntax_and_semantics/literals/hash.md)
       * [Range](syntax_and_semantics/literals/range.md)
       * [Regex](syntax_and_semantics/literals/regex.md)
       * [Tuple](syntax_and_semantics/literals/tuple.md)
       * [NamedTuple](syntax_and_semantics/literals/named_tuple.md)
       * [Proc](syntax_and_semantics/literals/proc.md)
   * [Atribuição](syntax_and_semantics/assignment.md)
       * [Atribuição múltipla](syntax_and_semantics/multiple_assignment.md)
   * [Variáveis locais](syntax_and_semantics/local_variables.md)
   * [Variáveis globais](syntax_and_semantics/global_variables.md)
   * [Tipos união](syntax_and_semantics/union_types.md)
   * [Expressões de controle](syntax_and_semantics/control_expressions.md)
       * [Valores verdadeiros e falsos](syntax_and_semantics/truthy_and_falsey_values.md)
       * [if](syntax_and_semantics/if.md)
           * [Como um sufixo](syntax_and_semantics/as_a_suffix.md)
           * [Como uma expressão](syntax_and_semantics/as_an_expression.md)
           * [if ternário](syntax_and_semantics/ternary_if.md)
           * [if var](syntax_and_semantics/if_var.md)
           * [if var.is_a?(...)](syntax_and_semantics/if_varis_a.md)
           * [if var.responds_to?(...)](syntax_and_semantics/if_varresponds_to.md)
           * [if var.nil?](syntax_and_semantics/if_var_nil.md)
           * [if !](syntax_and_semantics/not.md)
       * [unless](syntax_and_semantics/unless.md)
       * [case](syntax_and_semantics/case.md)
       * [while](syntax_and_semantics/while.md)
           * [break](syntax_and_semantics/break.md)
           * [next](syntax_and_semantics/next.md)
       * [until](syntax_and_semantics/until.md)
       * [&&](syntax_and_semantics/and.md)
       * [||](syntax_and_semantics/or.md)
   * [Tipos e métodos](syntax_and_semantics/types_and_methods.md)
       * [Tudo é um objeto](syntax_and_semantics/everything_is_an_object.md)
       * [O Programa](syntax_and_semantics/the_program.md)
       * [Classes e métodos](syntax_and_semantics/classes_and_methods.md)
           * [new, initialize e allocate](syntax_and_semantics/new,_initialize_and_allocate.md)
           * [Métodos e variáveis de instância](syntax_and_semantics/methods_and_instance_variables.md)
           * [Inferência de tipo](syntax_and_semantics/type_inference.md)
           * [Overloading](syntax_and_semantics/overloading.md)
           * [Default values and named arguments](syntax_and_semantics/default_and_named_arguments.md)
           * [Splats and tuples](syntax_and_semantics/splats_and_tuples.md)
           * [Type restrictions](syntax_and_semantics/type_restrictions.md)
           * [Return types](syntax_and_semantics/return_types.md)
           * [Method arguments](syntax_and_semantics/default_values_named_arguments_splats_tuples_and_overloading.md)
           * [Operators](syntax_and_semantics/operators.md)
           * [Visibility](syntax_and_semantics/visibility.md)
           * [Inheritance](syntax_and_semantics/inheritance.md)
               * [Virtual and abstract types](syntax_and_semantics/virtual_and_abstract_types.md)
           * [Class variables](syntax_and_semantics/class_variables.md)
           * [finalize](syntax_and_semantics/finalize.md)
       * [Modules](syntax_and_semantics/modules.md)
       * [Generics](syntax_and_semantics/generics.md)
       * [Structs](syntax_and_semantics/structs.md)
       * [Constants](syntax_and_semantics/constants.md)
       * [Enums](syntax_and_semantics/enum.md)
       * [Blocks and Procs](syntax_and_semantics/blocks_and_procs.md)
           * [Capturing blocks](syntax_and_semantics/capturing_blocks.md)
           * [Proc literal](syntax_and_semantics/proc_literal.md)
           * [Block forwarding](syntax_and_semantics/block_forwarding.md)
           * [Closures](syntax_and_semantics/closures.md)
       * [alias](syntax_and_semantics/alias.md)
   * [Type reflection](syntax_and_semantics/type_reflection.md)
       * [is_a?](syntax_and_semantics/is_a.md)
       * [nil?](syntax_and_semantics/nil_question.md)
       * [responds_to?](syntax_and_semantics/responds_to.md)
       * [as](syntax_and_semantics/as.md)
       * [as?](syntax_and_semantics/as_question.md)
       * [typeof](syntax_and_semantics/typeof.md)
   * [Attributes](syntax_and_semantics/attributes.md)
   * [Requiring files](syntax_and_semantics/requiring_files.md)
   * [Low-level primitives](syntax_and_semantics/low_level_primitives.md)
       * [pointerof](syntax_and_semantics/pointerof.md)
       * [sizeof](syntax_and_semantics/sizeof.md)
       * [instance_sizeof](syntax_and_semantics/instance_sizeof.md)
       * [Uninitialized variable declaration](syntax_and_semantics/declare_var.md)
   * [Exception handling](syntax_and_semantics/exception_handling.md)
   * [Compile-time flags](syntax_and_semantics/compile_time_flags.md)
       * [Cross-compilation](syntax_and_semantics/cross-compilation.md)
   * [Macros](syntax_and_semantics/macros.md)
       * [Macro methods](syntax_and_semantics/macros/macro_methods.md)
       * [Hooks](syntax_and_semantics/macros/hooks.md)
       * [Fresh variables](syntax_and_semantics/macros/fresh_variables.md)
   * [C bindings](syntax_and_semantics/c_bindings/README.md)
       * [lib](syntax_and_semantics/c_bindings/lib.md)
       * [fun](syntax_and_semantics/c_bindings/fun.md)
           * [out](syntax_and_semantics/c_bindings/out.md)
           * [to_unsafe](syntax_and_semantics/c_bindings/to_unsafe.md)
       * [struct](syntax_and_semantics/c_bindings/struct.md)
       * [union](syntax_and_semantics/c_bindings/union.md)
       * [enum](syntax_and_semantics/c_bindings/enum.md)
       * [Variables](syntax_and_semantics/c_bindings/variables.md)
       * [Constants](syntax_and_semantics/c_bindings/constants.md)
       * [type](syntax_and_semantics/c_bindings/type.md)
       * [alias](syntax_and_semantics/c_bindings/alias.md)
       * [Callbacks](syntax_and_semantics/c_bindings/callbacks.md)
   * [Type grammar](syntax_and_semantics/type_grammar.md)
   * [Unsafe code](syntax_and_semantics/unsafe.md)
* [Conventions](conventions/README.md)
   * [Coding style](conventions/coding_style.md)
   * [Documenting code](conventions/documenting_code.md)
* [Guides](guides/README.md)
   * [Performance](guides/performance.md)
   * [Concurrency](guides/concurrency.md)
