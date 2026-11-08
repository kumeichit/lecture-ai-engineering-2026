# 第3回 解答

## 演習

- 第1回（素のLLM）とエージェントの回答の違い：
＞正しい回答がかえされていることが、data/glossary/jsonと比較しすることで確認された。

- `--trace` で見えたツール呼び出し（ツール名と引数）：
[tool call]   search_glossary({'query': 'LoRA'})
[tool call]   search_glossary({'query': 'QLoRA'})
[tool return] search_glossary -> [{"term": "LoRA", "lecture": 2, "definition": 
[tool return] search_glossary -> [{"term": "QLoRA", "lecture": 2, "definition": 

- 1つの質問での LLM 呼び出し回数（`requests`）：
呼び出し回数＞２回
[usage] RunUsage(cost=Decimal('0.0007963'), details={'text_prompt_tokens': 1196}, input_text_tokens=1196, input_tokens=1196, output_tokens=175, requests=2, tool_calls=2)

- 追加したツールと、docstring に書いた説明：
追加したツール＞search_glossary
docstring の説明
    """講座の用語集から用語を検索し、定義と、どの回で扱うかを返す。
    AIエンジニアリングの用語や、この講座（AIE2026）に固有の言葉について
    答える前に使うこと。query には調べたい用語を1つだけ入れる（例: "LoRA"）。
    """


## 宿題

- 取り組んだレベル：基礎 / 実装 / 発展
- やったこと：
- 結果：
- 気づき・疑問：
