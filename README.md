# MappingTool
Illumina Paired Sequence mapping, bed-filed trim, trimmed sequence out.

## これはなに？
iVar(https://andersen-lab.github.io/ivar/html/manualpage.html)を利用し
Windows 上で 簡単に操作できるよう UI を付けたツールです。

Illumina Sequencer では Primer 情報があり、bed-file が得られる（はず）なので、
マッピング結果から bed-file を利用したtrim が出来ないかと考えた。  
iVar が Corona Virus のシーケンスに利用されていたのでWindows でも容易に
使えないかと考えたので 作ってみた。  
  
  
Reference fasta、Illumina Pair-end Sequence と、bed-file を入力として以下を出力します。  
１．Minimap2(https://github.com/lh3/minimap2)でマッピング  
２．iVar trim で マッピング結果(bam)をTrim  
３．iVar variant で バリアント.tsv を出力  
４．samtools(http://www.htslib.org/) で Trimしたbam から Fastq を作成  
  
## 使い方。
このレポジトリをzip ファイルで取得（もしくは git clone）  
Windows PC の スペース、日本語などを含まないフォルダに解凍（or Clone）  
iVarWrapper.exe をダブルクリックすると起動します。
  
レジストリなどの登録はありません。  
解凍したフォルダを削除することでアンインストールとなります。  

## 技術とか。
Windows WPF
Livet https://github.com/runceel/Livet

## Windows binary compile
MinGW(https://www.mingw-w64.org/)
・samtools
・iVar
・minimap2

## 連絡先
techsupport＠w-fusion.co.jp
アットマークは全角です。半角に直してください

## TODO
IGV を同梱しようかと思ったけどjre のファイル数が多くて断念。
なにか mapping 結果を見るツールをいれたい。

RabbitQC(https://github.com/ZekunYin/RabbitQC)
最初のマッピング前に入れる

## 要望とか。
Bio ツールは Pythonで動くとか、Linux のコマンドとかが中心です。
Windows で簡単に操作できればいいのに と、言ったツールがあれば連絡ください。
