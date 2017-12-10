# ios-swiftlint-rules
SwiftLintのルール

## disabled_rules
デフォルト有効となっているルール

| identifier | opt-in | 説明 | 無効設定 | 無効にする理由 |
|-----------|:------------:|------------|:-----------:|:------------:|
| block_based_kvo                          | no ||||
| class_delegate_protocol                  | no |Protcolはweakで保持される可能性があるため、class-onlyなProtocolにすべき|||
| closing_brace                            | no |}の後に)が続く場合、間に空白があるべきでない|||
| closure_parameter_position               | no |クロージャの引数リストはクロージャの始まり{と同じ行にあるべき|||
| colon                                    | no |:は変数名の直後に書き、型名はその後に1スペース開けて書くべき|||
| comma                                    | no |,の前にはスペースを入れず、,の後には1つのスペースを入れるべき|||
| compiler_protocol_init                   | no |リテラルを直接書き並べて初期化するタイプのinitializerは直接呼び出すべきではない|||
| control_statement                        | no |if等の制御文の条件式部分は( )で囲むべきでない|||
| custom_rules                             | no ||||
| cyclomatic_complexity                    | no |関数内の複雑度は下げるべき(ifやswitchの連続、ループ内の条件分岐)|||
| discarded_notification_center_observer   | no ||||
| discouraged_direct_init                  | no |NotificationCenter.addObserver(forName:object:queue:using:)で追加されたobserverは後で除去できるように変数に格納して保持するべき|||
| dynamic_inline                           | no |@inline指定とdynamicを同時に使うべきでない|||
| empty_enum_arguments                     | no |末尾クロージャを使用するときはメソッド名の後に引数のない空の()は書くべきでない|||
| empty_parameters                         | no |関数の引数がない時，Void ->でなく() ->を用いるべき|||
| empty_parentheses_with_trailing_closure  | no |末尾クロージャを使用するときはメソッド名の後に引数のない空の()は書くべきでない|||
| fallthrough                              | no ||||
| file_length                              | no |ファイルの行数は多くなりすぎないようにすべき|||
| for_where                                | no |for文において、その内部でifによる値チェック処理しかしないのであればwhere句を使用すべき|||
| force_cast                               | no |強制キャスト(as!)は避けるべき|||
| force_try                                | no |try!の使用は避けるべき|||
| function_body_length                     | no |関数の行数は長くすべきでない(41行以上)|||
| function_parameter_count                 | no |関数の引数は少なくすべき(6個以内）|||
| generic_type_name                        | no |ジェネリクスの型名は大文字のアルファベットから初めて、英数字のみを含み、かつ1〜20文字の長さにするべき|||
| identifier_name                          | no |変数名等の識別子は小文字で始まるか全て大文字の英数字だけで構成させるべき|||
| implicit_getter                          | no |read-onlyな計算プロパティはgetキーワードを書くべきでない|||
| is_disjoint                              | no ||||
| large_tuple                              | no |タプルのメンバは少なめにすべき|||
| leading_whitespace                       | no |ファイルの先頭に空白類文字を含むべきでない|||
| legacy_cggeometry_functions              | no ||||
| legacy_constant                          | no ||||
| legacy_constructor                       | no ||||
| legacy_nsgeometry_functions              | no ||||
| line_length                              | no |1行における文字数は多くなりすぎないようにすべき|||
| mark                                     | no |MARKコメントは正しいフォーマットで書くべき|||
| multiple_closures_with_trailing_closure  | no ||||
| nesting                                  | no |ネスト型は深くても1レベルの深さまで、その他の文は深くても5レベルの深さまでのネストに留めるべき|||
| notification_center_detachment           | no |NSNotificationCenterに登録したobserverはクラスのdeinit内で除去するべき|||
| opening_brace                            | no |関数等の開き{は直前に1つのスペースを置いてから書き、なおかつ宣言と同じ行に書くべき|||
| operator_whitespace                      | no |演算子を定義する際は演算子の前後に1つのスペースを置くべき|||
| private_over_fileprivate                 | no |トップレベルにあるfileprivateはprivateにするべき|||
| private_unit_test                        | no |privateなテストケースメソッドは書かない|||
| protocol_property_accessors_order        | no ||||
| redundant_discardable_let                | no |関数の戻り値を参照しない場合、letはわざわざ書くべきではない|||
| redundant_optional_initialization        | no |オプショナル変数宣言時のnil初期化は冗長なため、書くべきでない|||
| redundant_string_enum_value              | no |String型のenumの各caseの値をcase名と同じにする際は、その処理は省略できるので書くべきでない|||
| redundant_void_return                    | no |Voidを返す関数の宣言時に-> Voidを書くのは冗長なため、書くべきでない|||
| return_arrow_whitespace                  | no |関数の戻り値を指定する->と型名は、それぞれ1つのスペースで区切られるか、別の行に書くべき|||
| shorthand_operator                       | no |複号代入演算子をなるべく使うべき|||
| statement_position                       | no |else節やcatch節は直前の}の後に1つのスペースを置き，同じ行に書くべき|||
| superfluous_disable_command              | no ||||
| switch_case_alignment                    | no ||||
| syntactic_sugar                          | no |糖衣構文を使うべき|||
| todo                                     | no |TODOおよびFIXMEコメントは避けるべき|||
| trailing_comma                           | no |ArrayやDictionary中の末尾の,は避ける/強制すべき|||
| trailing_newline                         | no |各ファイルは末尾に空行を1行だけ持つべき|||
| trailing_semicolon                       | no |各行の末尾にセミコロンは書くべきでない|||
| trailing_whitespace                      | no |各行の末尾に空白類文字を書くべきでない|||
| type_body_length                         | no |型の本体の行数は多くなりすぎないようにすべき|||
| type_name                                | no |型名は大文字アルファベットで始まる英数字だけで構成され、かつ3~40文字であるべき|||
| unneeded_break_in_switch                 | no ||||
| unused_closure_parameter                 | no |使用されないクロージャの引数は_で置き換えるべき|||
| unused_enumerated                        | no |for文でindexないしは要素が使用されないときは.enumerated()の記述は除去できるので除去すべき|||
| unused_optional_binding                  | no |let _ =によるOptional Bindingではなく、!= nilでOptional判定するべき|||
| valid_ibinspectable                      | no |@IBInspectable属性は明示的な型を持った変数とサポートされた型にのみ用いるべき|||
| vertical_parameter_alignment             | no |関数の引数を複数行に分けて書く際は位置を揃えるべき|||
| vertical_whitespace                      | no |空行は1行に抑えるべき|||
| void_return                              | no |-> ()ではなく、-> Voidを用いるべき|||
| weak_delegate                            | no |循環参照を避けるため、Delegateはweakで保持されるべき|||
| xctfail_message                          | no |XCTFailを呼び出す場合、アサーションの説明を記載するべき|||


## opt_in_rules
デフォルト無効となっているルール

| identifier | opt-in | 説明 | 有効設定 | 有効にする理由 |
|-----------|:------------:|------------|:-----------:|:------------:|
| array_init                               | yes ||||
| attributes                               | yes ||||
| closure_end_indentation                  | yes ||||
| closure_spacing                          | yes |クロージャ内の式はカッコの間に1つのスペースがあるべき|||
| conditional_returns_on_newline           | yes |条件文は始まった行の次の行でreturnするべき|○||
| contains_over_first_not_nil              | yes ||||
| empty_count                              | yes |要素が何もないことを確認する際はcount == 0よりもisEmptyを用いるべき|○||
| explicit_enum_raw_value                  | yes ||||
| explicit_init                            | yes |明示的な.init()メソッドの呼び出しは避けるべき|○||
| explicit_top_level_acl                   | yes ||||
| explicit_type_interface                  | yes ||||
| extension_access_modifier                | yes ||||
| fatal_error_message                      | yes ||||
| file_header                              | yes |各ファイルは一貫性のあるヘッダコメントを持つべき|○||
| first_where                              | yes |.filter { }.firstよりも.first(where:)を用いべき|○||
| force_unwrapping                         | yes |強制アンラップは避けるべき|○||
| implicit_return                          | yes ||||
| implicitly_unwrapped_optional            | yes ||||
| joined_default_parameter                 | yes ||||
| let_var_whitespace                       | yes ||||
| literal_expression_end_indentation       | yes ||||
| multiline_arguments                      | yes ||||
| multiline_parameters                     | yes ||||
| nimble_operator                          | yes ||||
| no_extension_access_modifier             | yes ||||
| no_grouping_extension                    | yes ||||
| number_separator                         | yes |桁数の多い数値を書く際はセパレータを書くべき(1_000_000)|||
| object_literal                           | yes |イニシャライザを直接呼び出すよりは#imageLiteralや#colorLiteralを用いるべき|○||
| operator_usage_whitespace                | yes |演算子を使用する際は前後に1つのスペースを開けるべき|○||
| overridden_super_call                    | yes |オーバーライドされたメソッドは常にsuperを呼び出すべき|○||
| override_in_extension                    | yes |extension内では、オーバーライドするべきでない|○||
| pattern_matching_keywords                | yes ||||
| private_outlet                           | yes |@IBOutlet変数はprivate修飾するべき|○||
| prohibited_super_call                    | yes ||||
| quick_discouraged_call                   | yes ||||
| quick_discouraged_focused_test           | yes ||||
| quick_discouraged_pending_test           | yes ||||
| redundant_nil_coalescing                 | yes |nil結合演算子において、左辺がnilの場合のみ評価される性質上、右辺にnilを書くのは冗長なため、書くべきでない|||
| single_test_class                        | yes |テストファイルには、単一のQuickSpec or XCTestCaseクラスを含むべき|||
| sorted_first_last                        | yes ||||
| sorted_imports                           | yes |import部分はソートされているべき|○||
| strict_fileprivate                       | yes ||||
| switch_case_on_newline                   | yes |switch文におけるcaseの各処理は改行した後書くべき|||
| trailing_closure                         | yes ||||
| unneeded_parentheses_in_closure_argument | yes ||||
| vertical_parameter_alignment_on_call     | yes ||||
