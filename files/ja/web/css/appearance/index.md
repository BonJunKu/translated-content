---
title: 'appearance (-moz-appearance, -webkit-appearance)'
slug: Web/CSS/appearance
tags:
  - '-moz-appearance'
  - '-webkit-appearance'
  - CSS
  - CSS プロパティ
  - CSS 基本ユーザーインターフェイス
  - Reference
  - appearance
translation_of: Web/CSS/appearance
---
<div>{{CSSRef}}{{SeeCompatTable}}</div>

<p>CSS の <strong><code>-moz-appearance</code></strong> プロパティは、 OS のテーマに基づいたプラットフォームネイティブのスタイル付けを使用して要素を表示するために、 Gecko (Firefox) によって使用されます。</p>

<p><strong><code>-webkit-appearance</code></strong> プロパティは、 WebKit ベースのブラウザー (Safari など) と Blink ベースのブラウザー (Chrome, Opera など) で同じことを実現するために使用されます。なお、 Firefox や Edge もまた、互換性の理由から <code>-webkit-appearance</code> に対応しています。</p>

<div>{{EmbedInteractiveExample("pages/css/appearance.html")}}</div>

<p class="hidden">このデモのソースファイルは GitHub リポジトリに格納されています。デモプロジェクトに協力したい場合は、 <a href="https://github.com/mdn/interactive-examples">https://github.com/mdn/interactive-examples</a> をクローンしてプルリクエストを送信してください。</p>

<p>このプロパティは <a href="/ja/docs/Mozilla/Tech/XUL/Tutorial">XUL</a> スタイルシート内で、プラットフォーム固有のカスタムウィジェットをデザインするために頻繁に使用されます。また、 Mozilla プラットフォームに搭載するウィジェットの <a href="/ja/docs/XBL">XBL</a> 実装でも使用されます。</p>

<div class="note">
<p><strong>互換性メモ</strong>: ウェブサイトでこのプロパティを使いたいのであれば、とても注意深くテストする必要があります。現在のブラウザーのほとんどは対応していますが、その実装は大きく異なります。古いブラウザーでは、 <code>none</code> キーワードであっても、ブラウザーによってフォーム要素すべてに同じ効果があるわけではなく、まったく対応していないものもあります。最新のブラウザーでは、その差は小さくなっています。</p>
</div>

<h2 id="Syntax" name="Syntax">構文</h2>

<pre class="brush: css">/* CSS 基本ユーザーインターフェイス Level 4 の値 */
appearance: none;
appearance: auto;
appearance: button;
appearance: textfield;
appearance: searchfield;
appearance: textarea;
appearance: push-button;
appearance: button-bevel;
appearance: slider-horizontal;
appearance: checkbox;
appearance: radio;
appearance: square-button;
appearance: menulist;
appearance: menulist-button;
appearance: listbox;
appearance: meter;
appearance: progress-bar;

/* Gecko で使用できる値の一部 */
-moz-appearance: scrollbarbutton-up;
-moz-appearance: button-bevel;

/* WebKit/Blink (Gecko や Edge も同様) で使用できる値の一部 */
-webkit-appearance: media-mute-button;
-webkit-appearance: caret;
</pre>

<p><code>-moz-appearance</code> プロパティは、以下の一覧から一つの値を選択して指定することができます。</p>

<h3 id="Values" name="Values">値</h3>

<p><code>&lt;appearance&gt;</code> は以下のキーワードのうちの一つです。</p>

<table class="standard-table">
 <tbody>
  <tr>
   <th>値</th>
   <th>デモ</th>
   <th>ブラウザー</th>
   <th>説明</th>
  </tr>
  <tr>
   <td><code>none</code></td>
   <td>
    <div class="hidden" id="sampleNone">
    <pre class="brush: css">
div{ color: black;
-moz-appearance:none;
-webkit-appearance:none;
appearance:none; }</pre>

    <pre class="brush: html">
&lt;div&gt;Lorem&lt;/div&gt;</pre>
    </div>
    {{EmbedLiveSample("sampleNone",100,50,"","", "nobutton")}}</td>
   <td>Firefox Chrome Safari Edge</td>
   <td>特別なスタイルは適用されません。これが既定です。</td>
  </tr>
  <tr>
   <td><code>auto</code> {{Experimental_Inline}}</td>
   <td>
    <div class="hidden" id="sampleAuto">
    <pre class="brush: css">
div{ color: black;
-moz-appearance: auto;
-webkit-appearance: auto;
appearance:auto; }</pre>

    <pre class="brush: html">
&lt;div&gt;Lorem&lt;/div&gt;</pre>
    </div>
    {{EmbedLiveSample("sampleAuto",100,50,"","", "nobutton")}}</td>
   <td>なし</td>
   <td>ユーザーエージェントが要素に基づいて適切で特別なスタイルを選択します。特別なスタイルがない要素では <code>none</code> として動作します。</td>
  </tr>
  <tr>
   <td><code>attachment</code> {{Non-standard_Inline}}</td>
   <td>
    <div class="hidden" id="sampleAttachment">
    <pre class="brush: css">
div{ color: black;
-moz-appearance: attachment;
-webkit-appearance: attachment; }</pre>

    <pre class="brush: html">
&lt;div&gt;Lorem&lt;/div&gt;</pre>
    </div>
    {{EmbedLiveSample("sampleAttachment",100,50,"","", "nobutton")}}</td>
   <td>Safari</td>
   <td></td>
  </tr>
  <tr>
   <td><code>borderless-attachment</code> {{Non-standard_Inline}}</td>
   <td>
    <div class="hidden" id="sample-borderless-attachment">
    <pre class="brush: css">
div{ color: black;
-moz-appearance: borderless-attachment;
-webkit-appearance: borderless-attachment; }</pre>

    <pre class="brush: html">
&lt;div&gt;Lorem&lt;/div&gt;</pre>
    </div>
    {{EmbedLiveSample("sample-borderless-attachment",100,50,"","","nobutton")}}</td>
   <td>Safari</td>
   <td></td>
  </tr>
  <tr>
   <td><code>button</code> {{Non-standard_Inline}}</td>
   <td>
    <div class="hidden" id="sampleButton">
    <pre class="brush: css">
div { color: black;
-moz-appearance: button;
-webkit-appearance: button; }</pre>

    <pre class="brush: html">
&lt;div&gt;Lorem&lt;/div&gt;</pre>
    </div>
    {{EmbedLiveSample("sampleButton",100,50,"","", "nobutton")}}</td>
   <td>Firefox Chrome Safari Edge</td>
   <td>要素がボタンのように描画されます。</td>
  </tr>
  <tr>
   <td><code>button-arrow-down</code> {{Non-standard_Inline}}</td>
   <td>
    <div class="hidden" id="sampleButtonArrowDown">
    <pre class="brush: css">
div { color: black;
-moz-appearance: button-arrow-down;
-webkit-appearance: button-arrow-down; }</pre>

    <pre class="brush: html">
&lt;div&gt;Lorem&lt;/div&gt;</pre>
    </div>
    {{EmbedLiveSample("sampleButtonArrowDown",100,50,"","", "nobutton")}}</td>
   <td>Firefox</td>
   <td>Firefox 64 で削除</td>
  </tr>
  <tr>
   <td><code>button-arrow-next</code> {{Non-standard_Inline}}</td>
   <td>
    <div class="hidden" id="sampleButtonArrowNext">
    <pre class="brush: css">
div { color: black;
-moz-appearance: button-arrow-next;
-webkit-appearance: button-arrow-next; }</pre>

    <pre class="brush: html">
&lt;div&gt;Lorem&lt;/div&gt;</pre>
    </div>
    {{EmbedLiveSample("sampleButtonArrowNext",100,50,"","", "nobutton")}}</td>
   <td>Firefox</td>
   <td>Firefox 64 で削除</td>
  </tr>
  <tr>
   <td><code>button-arrow-previous</code> {{Non-standard_Inline}}</td>
   <td>
    <div class="hidden" id="sampleButtonArrowPrevious">
    <pre class="brush: css">
div { color: black;
-moz-appearance: button-arrow-previous;
-webkit-appearance: button-arrow-previous; }</pre>

    <pre class="brush: html">
&lt;div&gt;Lorem&lt;/div&gt;</pre>
    </div>
    {{EmbedLiveSample("sampleButtonArrowPrevious",100,50,"","", "nobutton")}}</td>
   <td>Firefox</td>
   <td>Firefox 64 で削除</td>
  </tr>
  <tr>
   <td><code>button-arrow-up</code> {{Non-standard_Inline}}</td>
   <td>
    <div class="hidden" id="sampleButtonArrowUp">
    <pre class="brush: css">
div { color: black;
-moz-appearance: button-arrow-up;
-webkit-appearance: button-arrow-up; }</pre>

    <pre class="brush: html">
&lt;div&gt;Lorem&lt;/div&gt;</pre>
    </div>
    {{EmbedLiveSample("sampleButtonArrowUp",100,50,"","", "nobutton")}}</td>
   <td>Firefox</td>
   <td>Firefox 64 で削除</td>
  </tr>
  <tr>
   <td><code>button-bevel</code> {{Non-standard_Inline}}</td>
   <td>
    <div class="hidden" id="sampleButtonBevel">
    <pre class="brush: css">
div { color: black;
-moz-appearance: button-bevel;
-webkit-appearance: button-bevel; }</pre>

    <pre class="brush: html">
&lt;div&gt;Lorem&lt;/div&gt;</pre>
    </div>
    {{EmbedLiveSample("sampleButtonBevel",100,50,"","", "nobutton")}}</td>
   <td>Firefox Chrome Safari Edge</td>
   <td></td>
  </tr>
  <tr>
   <td><code>button-focus</code> {{Non-standard_Inline}}</td>
   <td>
    <div class="hidden" id="sampleButtonFocus">
    <pre class="brush: css">
div { color: black;
-moz-appearance: button-focus;
-webkit-appearance: button-focus; }</pre>

    <pre class="brush: html">
&lt;div&gt;Lorem&lt;/div&gt;</pre>
    </div>
    {{EmbedLiveSample("sampleButtonFocus",100,50,"","", "nobutton")}}</td>
   <td>Firefox</td>
   <td>Firefox 64 で削除</td>
  </tr>
  <tr>
   <td><code>caps-lock-indicator</code> {{Non-standard_Inline}}</td>
   <td>
    <div class="hidden" id="sample-caps-lock-indicator">
    <pre class="brush: css">
div{ color: black;
-moz-appearance: caps-lock-indicator;
-webkit-appearance: caps-lock-indicator; }</pre>

    <pre class="brush: html">
&lt;div&gt;Lorem&lt;/div&gt;</pre>
    </div>
    {{EmbedLiveSample("sample-caps-lock-indicator",100,50,"","","nobutton")}}</td>
   <td>Safari Edge</td>
   <td></td>
  </tr>
  <tr>
   <td><code>caret</code> {{Non-standard_Inline}}</td>
   <td>
    <div class="hidden" id="sampleCaret">
    <pre class="brush: css">
div { color: black;
-moz-appearance: caret;
-webkit-appearance: caret; }</pre>

    <pre class="brush: html">
&lt;div&gt;Lorem&lt;/div&gt;</pre>
    </div>
    {{EmbedLiveSample("sampleCaret",100,50,"","", "nobutton")}}</td>
   <td>Firefox Chrome Safari Edge</td>
   <td></td>
  </tr>
  <tr>
   <td><code>checkbox</code> {{Non-standard_Inline}}</td>
   <td>
    <div class="hidden" id="sampleCheckbox">
    <pre class="brush: css">
div { color: black;
-moz-appearance: checkbox;
-webkit-appearance: checkbox; }</pre>

    <pre class="brush: html">
&lt;div&gt;Lorem&lt;/div&gt;</pre>
    </div>
    {{EmbedLiveSample("sampleCheckbox",100,50,"","", "nobutton")}}</td>
   <td>Firefox Chrome Safari Edge</td>
   <td>要素がチェックボックスのように描画されます。実際の "checkbox" 部分のみを含みます。</td>
  </tr>
  <tr>
   <td><code>checkbox-container</code> {{Non-standard_Inline}}</td>
   <td>
    <div class="hidden" id="sampleCheckboxContainer">
    <pre class="brush: css">
div { color: black;
-moz-appearance: checkbox-container;
-webkit-appearance: checkbox-container; }</pre>

    <pre class="brush: html">
&lt;div&gt;Lorem&lt;/div&gt;</pre>
    </div>
    {{EmbedLiveSample("sampleCheckboxContainer",100,50,"","", "nobutton")}}</td>
   <td>Firefox</td>
   <td>要素がチェックボックスのコンテナのように描画されます。あるプラットフォーム下では背景の発光効果を含みます。通常はラベルとチェックボックスを含みます。</td>
  </tr>
  <tr>
   <td><code>checkbox-label</code> {{Non-standard_Inline}}</td>
   <td>
    <div class="hidden" id="sampleCheckboxLabel">
    <pre class="brush: css">
div { color: black;
-moz-appearance: checkbox-label;
-webkit-appearance: checkbox-label; }</pre>

    <pre class="brush: html">
&lt;div&gt;Lorem&lt;/div&gt;</pre>
    </div>
    {{EmbedLiveSample("sampleCheckboxLabel",100,50,"","", "nobutton")}}</td>
   <td>Firefox</td>
   <td></td>
  </tr>
  <tr>
   <td><code>checkmenuitem</code> {{Non-standard_Inline}}</td>
   <td>
    <div class="hidden" id="sampleCheckmenuitem">
    <pre class="brush: css">
div { color: black; height: 20px;
-moz-appearance: checkmenuitem;
-webkit-appearance: checkmenuitem; }</pre>

    <pre class="brush: html">
&lt;div&gt;Lorem&lt;/div&gt;</pre>
    </div>
    {{EmbedLiveSample("sampleCheckmenuitem",100,50,"","", "nobutton")}}</td>
   <td>Firefox</td>
   <td></td>
  </tr>
  <tr>
   <td><code>color-well</code> {{Non-standard_Inline}}</td>
   <td>
    <div class="hidden" id="sample-color-well">
    <pre class="brush: css">
div{ color: black;
-moz-appearance: color-well;
-webkit-appearance: color-well; }</pre>

    <pre class="brush: html">
&lt;div&gt;Lorem&lt;/div&gt;</pre>
    </div>
    {{EmbedLiveSample("sample-color-well",100,50,"","","nobutton")}}</td>
   <td>Safari</td>
   <td><code>input type=color</code></td>
  </tr>
  <tr>
   <td><code>continuous-capacity-level-indicator</code> {{Non-standard_Inline}}</td>
   <td>
    <div class="hidden" id="sample-continuous-capacity-level-indicator">
    <pre class="brush: css">
div{ color: black;
-moz-appearance: continuous-capacity-level-indicator;
-webkit-appearance: continuous-capacity-level-indicator; }</pre>

    <pre class="brush: html">
&lt;div&gt;Lorem&lt;/div&gt;</pre>
    </div>
    {{EmbedLiveSample("sample-continuous-capacity-level-indicator",100,50,"","","nobutton")}}</td>
   <td>Safari</td>
   <td></td>
  </tr>
  <tr>
   <td><code>default-button</code> {{Non-standard_Inline}}</td>
   <td>
    <div class="hidden" id="sample-default-button">
    <pre class="brush: css">
div{ color: black;
-moz-appearance: default-button;
-webkit-appearance: default-button; }</pre>

    <pre class="brush: html">
&lt;div&gt;Lorem&lt;/div&gt;</pre>
    </div>
    {{EmbedLiveSample("sample-default-button",100,50,"","","nobutton")}}</td>
   <td>Safari Edge</td>
   <td></td>
  </tr>
  <tr>
   <td><code>discrete-capacity-level-indicator</code> {{Non-standard_Inline}}</td>
   <td>
    <div class="hidden" id="sample-discrete-capacity-level-indicator">
    <pre class="brush: css">
div{ color: black;
-moz-appearance: discrete-capacity-level-indicator;
-webkit-appearance: discrete-capacity-level-indicator; }</pre>

    <pre class="brush: html">
&lt;div&gt;Lorem&lt;/div&gt;</pre>
    </div>
    {{EmbedLiveSample("sample-discrete-capacity-level-indicator",100,50,"","","nobutton")}}</td>
   <td>Safari</td>
   <td></td>
  </tr>
  <tr>
   <td><code>dualbutton</code> {{Non-standard_Inline}}</td>
   <td>
    <div class="hidden" id="sampleDualButton">
    <pre class="brush: css">
div { color: black;
-moz-appearance: dualbutton;
-webkit-appearance: dualbutton; }</pre>

    <pre class="brush: html">
&lt;div&gt;Lorem&lt;/div&gt;</pre>
    </div>
    {{EmbedLiveSample("sampleDualButton",100,50,"","", "nobutton")}}</td>
   <td>Firefox</td>
   <td>Firefox 64 で削除</td>
  </tr>
  <tr>
   <td><code>groupbox</code> {{Non-standard_Inline}}</td>
   <td>
    <div class="hidden" id="sampleGroupbox">
    <pre class="brush: css">
div { color: black;
-moz-appearance: groupbox;
-webkit-appearance: groupbox; }</pre>

    <pre class="brush: html">
&lt;div&gt;Lorem&lt;/div&gt;</pre>
    </div>
    {{EmbedLiveSample("sampleGroupbox",100,50,"","", "nobutton")}}</td>
   <td>Firefox</td>
   <td>Firefox 64 で削除</td>
  </tr>
  <tr>
   <td><code>inner-spin-button</code> {{Non-standard_Inline}}</td>
   <td>
    <div class="hidden" id="sampleInnerSpinButton">
    <pre class="brush: css">
div{ color: black;
-webkit-appearance: inner-spin-button; }</pre>

    <pre class="brush: html">
&lt;div&gt;Lorem&lt;/div&gt;</pre>
    </div>
    {{EmbedLiveSample("sampleInnerSpinButton",100,50,"","", "nobutton")}}</td>
   <td>Firefox Chrome Safari</td>
   <td></td>
  </tr>
  <tr>
   <td><code>image-controls-button</code> {{Non-standard_Inline}}</td>
   <td>
    <div class="hidden" id="sample-image-controls-button">
    <pre class="brush: css">
div{ color: black;
-moz-appearance: image-controls-button;
-webkit-appearance: image-controls-button; }</pre>

    <pre class="brush: html">
&lt;div&gt;Lorem&lt;/div&gt;</pre>
    </div>
    {{EmbedLiveSample("sample-image-controls-button",100,50,"","","nobutton")}}</td>
   <td>Safari</td>
   <td></td>
  </tr>
  <tr>
   <td><code>list-button</code> {{Non-standard_Inline}}</td>
   <td>
    <div class="hidden" id="sample-list-button">
    <pre class="brush: css">
div{ color: black;
-moz-appearance: list-button;
-webkit-appearance: list-button; }</pre>

    <pre class="brush: html">
&lt;div&gt;Lorem&lt;/div&gt;</pre>
    </div>
    {{EmbedLiveSample("sample-list-button",100,50,"","","nobutton")}}</td>
   <td>Safari</td>
   <td>datalist</td>
  </tr>
  <tr>
   <td><code>listbox</code> {{Non-standard_Inline}}</td>
   <td>
    <div class="hidden" id="sampleListBox">
    <pre class="brush: css">
div { color: black; height:20px;
-moz-appearance: listbox;
-webkit-appearance: listbox; }</pre>

    <pre class="brush: html">
&lt;div&gt;Lorem&lt;/div&gt;</pre>
    </div>
    {{EmbedLiveSample("sampleListBox",100,50,"","", "nobutton")}}</td>
   <td>Firefox Chrome Safari Edge</td>
   <td></td>
  </tr>
  <tr>
   <td><code>listitem</code> {{Non-standard_Inline}}</td>
   <td>
    <div class="hidden" id="sampleListItem">
    <pre class="brush: css">
div { color: black;
-moz-appearance: listitem;
-webkit-appearance: listitem; }</pre>

    <pre class="brush: html">
&lt;div&gt;Lorem&lt;/div&gt;</pre>
    </div>
    {{EmbedLiveSample("sampleListItem",100,50,"","", "nobutton")}}</td>
   <td>Firefox Chrome Safari Edge</td>
   <td></td>
  </tr>
  <tr>
   <td><code>media-enter-fullscreen-button</code> {{Non-standard_Inline}}</td>
   <td>
    <div class="hidden" id="sampleMediaEnterFullscreenButton">
    <pre class="brush: css">
div{ color: black;
-webkit-appearance: media-enter-fullscreen-button; }</pre>

    <pre class="brush: html">
&lt;div&gt;Lorem&lt;/div&gt;</pre>
    </div>
    {{EmbedLiveSample("sampleMediaEnterFullscreenButton",100,50,"","", "nobutton")}}</td>
   <td>Chrome Safari</td>
   <td></td>
  </tr>
  <tr>
   <td><code>media-exit-fullscreen-button</code> {{Non-standard_Inline}}</td>
   <td>
    <div class="hidden" id="sampleMediaExitFullscreenButton">
    <pre class="brush: css">
div{ color: black;
-webkit-appearance: media-exit-fullscreen-button; }</pre>

    <pre class="brush: html">
&lt;div&gt;Lorem&lt;/div&gt;</pre>
    </div>
    {{EmbedLiveSample("sampleMediaExitFullscreenButton",100,50,"","", "nobutton")}}</td>
   <td>Chrome Safari</td>
   <td></td>
  </tr>
  <tr>
   <td><code>media-fullscreen-volume-slider</code> {{Non-standard_Inline}}</td>
   <td>
    <div class="hidden" id="sample-media-fullscreen-volume-slider">
    <pre class="brush: css">
div{ color: black;
-moz-appearance: media-fullscreen-volume-slider;
-webkit-appearance: media-fullscreen-volume-slider; }</pre>

    <pre class="brush: html">
&lt;div&gt;Lorem&lt;/div&gt;</pre>
    </div>
    {{EmbedLiveSample("sample-media-fullscreen-volume-slider",100,50,"","","nobutton")}}</td>
   <td>Safari</td>
   <td></td>
  </tr>
  <tr>
   <td><code>media-fullscreen-volume-slider-thumb</code> {{Non-standard_Inline}}</td>
   <td>
    <div class="hidden" id="sample-media-fullscreen-volume-slider-thumb">
    <pre class="brush: css">
div{ color: black;
-moz-appearance: media-fullscreen-volume-slider-thumb;
-webkit-appearance: media-fullscreen-volume-slider-thumb; }</pre>

    <pre class="brush: html">
&lt;div&gt;Lorem&lt;/div&gt;</pre>
    </div>
    {{EmbedLiveSample("sample-media-fullscreen-volume-slider-thumb",100,50,"","","nobutton")}}</td>
   <td>Safari</td>
   <td></td>
  </tr>
  <tr>
   <td><code>media-mute-button</code> {{Non-standard_Inline}}</td>
   <td>
    <div class="hidden" id="sampleMediaMuteButton">
    <pre class="brush: css">
div{ color: black;
-webkit-appearance: media-mute-button; }</pre>

    <pre class="brush: html">
&lt;div&gt;Lorem&lt;/div&gt;</pre>
    </div>
    {{EmbedLiveSample("sampleMediaMuteButton",100,50,"","", "nobutton")}}</td>
   <td>Chrome Safari Edge</td>
   <td></td>
  </tr>
  <tr>
   <td><code>media-play-button</code> {{Non-standard_Inline}}</td>
   <td>
    <div class="hidden" id="sampleMediaPlayButton">
    <pre class="brush: css">
div{ color: black;
-webkit-appearance: media-play-button; }</pre>

    <pre class="brush: html">
&lt;div&gt;Lorem&lt;/div&gt;</pre>
    </div>
    {{EmbedLiveSample("sampleMediaPlayButton",100,50,"","", "nobutton")}}</td>
   <td>Chrome Safari Edge</td>
   <td></td>
  </tr>
  <tr>
   <td><code>media-overlay-play-button</code> {{Non-standard_Inline}}</td>
   <td>
    <div class="hidden" id="sampleMediaOverlayPlayButton">
    <pre class="brush: css">
div{ color: black;
-webkit-appearance: media-overlay-play-button; }</pre>

    <pre class="brush: html">
&lt;div&gt;Lorem&lt;/div&gt;</pre>
    </div>
    {{EmbedLiveSample("sampleMediaOverlayPlayButton",100,50,"","", "nobutton")}}</td>
   <td>Chrome Safari</td>
   <td></td>
  </tr>
  <tr>
   <td><code>media-return-to-realtime-button</code> {{Non-standard_Inline}}</td>
   <td>
    <div class="hidden" id="sample-media-return-to-realtime-button">
    <pre class="brush: css">
div{ color: black;
-moz-appearance: media-return-to-realtime-button;
-webkit-appearance: media-return-to-realtime-button; }</pre>

    <pre class="brush: html">
&lt;div&gt;Lorem&lt;/div&gt;</pre>
    </div>
    {{EmbedLiveSample("sample-media-return-to-realtime-button",100,50,"","","nobutton")}}</td>
   <td>Safari</td>
   <td></td>
  </tr>
  <tr>
   <td><code>media-rewind-button</code> {{Non-standard_Inline}}</td>
   <td>
    <div class="hidden" id="sample-media-rewind-button">
    <pre class="brush: css">
div{ color: black;
-moz-appearance: media-rewind-button;
-webkit-appearance: media-rewind-button; }</pre>

    <pre class="brush: html">
&lt;div&gt;Lorem&lt;/div&gt;</pre>
    </div>
    {{EmbedLiveSample("sample-media-rewind-button",100,50,"","","nobutton")}}</td>
   <td>Safari</td>
   <td></td>
  </tr>
  <tr>
   <td><code>media-seek-back-button</code> {{Non-standard_Inline}}</td>
   <td>
    <div class="hidden" id="sample-media-seek-back-button">
    <pre class="brush: css">
div{ color: black;
-moz-appearance: media-seek-back-button;
-webkit-appearance: media-seek-back-button; }</pre>

    <pre class="brush: html">
&lt;div&gt;Lorem&lt;/div&gt;</pre>
    </div>
    {{EmbedLiveSample("sample-media-seek-back-button",100,50,"","","nobutton")}}</td>
   <td>Safari Edge</td>
   <td></td>
  </tr>
  <tr>
   <td><code>media-seek-forward-button</code> {{Non-standard_Inline}}</td>
   <td>
    <div class="hidden" id="sample-media-seek-forward-button">
    <pre class="brush: css">
div{ color: black;
-moz-appearance: media-seek-forward-button;
-webkit-appearance: media-seek-forward-button; }</pre>

    <pre class="brush: html">
&lt;div&gt;Lorem&lt;/div&gt;</pre>
    </div>
    {{EmbedLiveSample("sample-media-seek-forward-button",100,50,"","","nobutton")}}</td>
   <td>Safari Edge</td>
   <td></td>
  </tr>
  <tr>
   <td><code>media-toggle-closed-captions-button</code> {{Non-standard_Inline}}</td>
   <td>
    <div class="hidden" id="sampleMediaToggleClosedCaptionsButton">
    <pre class="brush: css">
div{ color: black;
-webkit-appearance: media-toggle-closed-captions-button; }</pre>

    <pre class="brush: html">
&lt;div&gt;Lorem&lt;/div&gt;</pre>
    </div>
    {{EmbedLiveSample("sampleMediaToggleClosedCaptionsButton",100,50,"","", "nobutton")}}</td>
   <td>Chrome Safari</td>
   <td></td>
  </tr>
  <tr>
   <td><code>media-slider</code> {{Non-standard_Inline}}</td>
   <td>
    <div class="hidden" id="sampleMediaSlider">
    <pre class="brush: css">
div{ color: black;
-webkit-appearance: media-slider; }</pre>

    <pre class="brush: html">
&lt;div&gt;Lorem&lt;/div&gt;</pre>
    </div>
    {{EmbedLiveSample("sampleMediaSlider",100,50,"","", "nobutton")}}</td>
   <td>Chrome Safari Edge</td>
   <td></td>
  </tr>
  <tr>
   <td><code>media-sliderthumb</code> {{Non-standard_Inline}}</td>
   <td>
    <div class="hidden" id="sampleMediaSliderThumb">
    <pre class="brush: css">
div{ color: black;
-webkit-appearance: media-sliderthumb; }</pre>

    <pre class="brush: html">
&lt;div&gt;Lorem&lt;/div&gt;</pre>
    </div>
    {{EmbedLiveSample("sampleMediaSliderThumb",100,50,"","", "nobutton")}}</td>
   <td>Chrome Safari Edge</td>
   <td></td>
  </tr>
  <tr>
   <td><code>media-volume-slider-container</code> {{Non-standard_Inline}}</td>
   <td>
    <div class="hidden" id="sampleMediaVolumeSliderContainer">
    <pre class="brush: css">
div{ color: black;
-webkit-appearance: media-volume-slider-container; }</pre>

    <pre class="brush: html">
&lt;div&gt;Lorem&lt;/div&gt;</pre>
    </div>
    {{EmbedLiveSample("sampleMediaVolumeSliderContainer",100,50,"","", "nobutton")}}</td>
   <td>Chrome Safari</td>
   <td></td>
  </tr>
  <tr>
   <td><code>media-volume-slider-mute-button</code> {{Non-standard_Inline}}</td>
   <td>
    <div class="hidden" id="sample-media-volume-slider-mute-button">
    <pre class="brush: css">
div{ color: black;
-moz-appearance: media-volume-slider-mute-button;
-webkit-appearance: media-volume-slider-mute-button; }</pre>

    <pre class="brush: html">
&lt;div&gt;Lorem&lt;/div&gt;</pre>
    </div>
    {{EmbedLiveSample("sample-media-volume-slider-mute-button",100,50,"","","nobutton")}}</td>
   <td>Safari</td>
   <td></td>
  </tr>
  <tr>
   <td><code>media-volume-slider</code> {{Non-standard_Inline}}</td>
   <td>
    <div class="hidden" id="sampleMediaVolumeSlider">
    <pre class="brush: css">
div{ color: black;
-webkit-appearance: media-volume-slider; }</pre>

    <pre class="brush: html">
&lt;div&gt;Lorem&lt;/div&gt;</pre>
    </div>
    {{EmbedLiveSample("sampleMediaVolumeSlider",100,50,"","", "nobutton")}}</td>
   <td>Chrome Safari</td>
   <td></td>
  </tr>
  <tr>
   <td><code>media-volume-sliderthumb</code> {{Non-standard_Inline}}</td>
   <td>
    <div class="hidden" id="sampleMediaVolumeSliderThumb">
    <pre class="brush: css">
div{ color: black;
-webkit-appearance: media-volume-slider-thumb; }</pre>

    <pre class="brush: html">
&lt;div&gt;Lorem&lt;/div&gt;</pre>
    </div>
    {{EmbedLiveSample("sampleMediaVolumeSliderThumb",100,50,"","", "nobutton")}}</td>
   <td>Chrome Safari</td>
   <td></td>
  </tr>
  <tr>
   <td><code>media-controls-background</code> {{Non-standard_Inline}}</td>
   <td>
    <div class="hidden" id="sampleMediaControlsBackground">
    <pre class="brush: css">
div{ color: black;
-webkit-appearance: media-controls-background; }</pre>

    <pre class="brush: html">
&lt;div&gt;Lorem&lt;/div&gt;</pre>
    </div>
    {{EmbedLiveSample("sampleMediaControlsBackground",100,50,"","", "nobutton")}}</td>
   <td>Chrome Safari</td>
   <td></td>
  </tr>
  <tr>
   <td><code>media-controls-dark-bar-background</code> {{Non-standard_Inline}}</td>
   <td>
    <div class="hidden" id="sample-media-controls-dark-bar-background">
    <pre class="brush: css">
div{ color: black;
-moz-appearance: media-controls-dark-bar-background;
-webkit-appearance: media-controls-dark-bar-background; }</pre>

    <pre class="brush: html">
&lt;div&gt;Lorem&lt;/div&gt;</pre>
    </div>
    {{EmbedLiveSample("sample-media-controls-dark-bar-background",100,50,"","","nobutton")}}</td>
   <td>Safari</td>
   <td></td>
  </tr>
  <tr>
   <td><code>media-controls-fullscreen-background</code> {{Non-standard_Inline}}</td>
   <td>
    <div class="hidden" id="sampleMediaControlsFullscreenBackground">
    <pre class="brush: css">
div{ color: black;
-webkit-appearance: media-controls-fullscreen-background; }</pre>

    <pre class="brush: html">
&lt;div&gt;Lorem&lt;/div&gt;</pre>
    </div>
    {{EmbedLiveSample("sampleMediaControlsFullscreenBackground",100,50,"","", "nobutton")}}</td>
   <td>Chrome Safari</td>
   <td></td>
  </tr>
  <tr>
   <td><code>media-controls-light-bar-background</code> {{Non-standard_Inline}}</td>
   <td>
    <div class="hidden" id="sample-media-controls-light-bar-background">
    <pre class="brush: css">
div{ color: black;
-moz-appearance: media-controls-light-bar-background;
-webkit-appearance: media-controls-light-bar-background; }</pre>

    <pre class="brush: html">
&lt;div&gt;Lorem&lt;/div&gt;</pre>
    </div>
    {{EmbedLiveSample("sample-media-controls-light-bar-background",100,50,"","","nobutton")}}</td>
   <td>Safari</td>
   <td></td>
  </tr>
  <tr>
   <td><code>media-current-time-display</code> {{Non-standard_Inline}}</td>
   <td>
    <div class="hidden" id="sampleMediaCurrentTimeDisplay">
    <pre class="brush: css">
div{ color: black;
-webkit-appearance: media-current-time-display; }</pre>

    <pre class="brush: html">
&lt;div&gt;Lorem&lt;/div&gt;</pre>
    </div>
    {{EmbedLiveSample("sampleMediaCurrentTimeDisplay",100,50,"","", "nobutton")}}</td>
   <td>Chrome Safari</td>
   <td></td>
  </tr>
  <tr>
   <td><code>media-time-remaining-display</code> {{Non-standard_Inline}}</td>
   <td>
    <div class="hidden" id="sampleMediaTimeRemainingDisplay">
    <pre class="brush: css">
div{ color: black;
-webkit-appearance: media-time-remaining-display; }</pre>

    <pre class="brush: html">
&lt;div&gt;Lorem&lt;/div&gt;</pre>
    </div>
    {{EmbedLiveSample("sampleMediaTimeRemainingDisplay",100,50,"","", "nobutton")}}</td>
   <td>Chrome Safari</td>
   <td></td>
  </tr>
  <tr>
   <td><code>menuarrow</code> {{Non-standard_Inline}}</td>
   <td>
    <div class="hidden" id="sampleMenuArrow">
    <pre class="brush: css">
div { color: black;
-moz-appearance: menuarrow;
-webkit-appearance: menuarrow; }</pre>

    <pre class="brush: html">
&lt;div&gt;Lorem&lt;/div&gt;</pre>
    </div>
    {{EmbedLiveSample("sampleMenuArrow",100,50,"","", "nobutton")}}</td>
   <td>Firefox</td>
   <td>Firefox 64 で削除</td>
  </tr>
  <tr>
   <td><code>menubar</code> {{Non-standard_Inline}}</td>
   <td>
    <div class="hidden" id="sampleMenubar">
    <pre class="brush: css">
div { color: balck;
-moz-appearance: menubar;
-webkit-appearance: menubar; }</pre>

    <pre class="brush: html">
&lt;div&gt;Lorem&lt;/div&gt;</pre>
    </div>
    {{EmbedLiveSample("sampleMenubar",100,50,"","", "nobutton")}}</td>
   <td>Firefox</td>
   <td>Firefox 64 で削除</td>
  </tr>
  <tr>
   <td><code>menucheckbox</code> {{Non-standard_Inline}}</td>
   <td>
    <div class="hidden" id="sampleMenuCheckbox">
    <pre class="brush: css">
div { color: black;
-moz-appearance: menucheckbox;
-webkit-appearance: menucheckbox; }</pre>

    <pre class="brush: html">
&lt;div&gt;Lorem&lt;/div&gt;</pre>
    </div>
    {{EmbedLiveSample("sampleMenuCheckbox",100,50,"","", "nobutton")}}</td>
   <td>Firefox</td>
   <td>Firefox 64 で削除</td>
  </tr>
  <tr>
   <td><code>menuimage</code> {{Non-standard_Inline}}</td>
   <td>
    <div class="hidden" id="sampleMenuImage">
    <pre class="brush: css">
div { color: black;
-moz-appearance: menuimage;
-webkit-appearance: menuimage; }</pre>

    <pre class="brush: html">
&lt;div&gt;Lorem&lt;/div&gt;</pre>
    </div>
    {{EmbedLiveSample("sampleMenuImage",100,50,"","", "nobutton")}}</td>
   <td>Firefox</td>
   <td>Firefox 64 で削除</td>
  </tr>
  <tr>
   <td><code>menuitem</code> {{Non-standard_Inline}}</td>
   <td>
    <div class="hidden" id="sampleMenuItem">
    <pre class="brush: css">
div { color: black;
-moz-appearance: menuitem;
-webkit-appearance: menuitem; }</pre>

    <pre class="brush: html">
&lt;div&gt;Lorem&lt;/div&gt;</pre>
    </div>
    {{EmbedLiveSample("sampleMenuItem",100,50,"","", "nobutton")}}</td>
   <td>Firefox</td>
   <td>Firefox 64 で削除。要素がメニュー項目としてスタイル付けられます。項目にマウスカーソルを合わせると強調されます。</td>
  </tr>
  <tr>
   <td><code>menuitemtext</code> {{Non-standard_Inline}}</td>
   <td>
    <div class="hidden" id="sampleMenuItemText">
    <pre class="brush: css">
div { color: black;
-moz-appearance: menuitemtext;
-webkit-appearance: menuitemtext; }</pre>

    <pre class="brush: html">
&lt;div&gt;Lorem&lt;/div&gt;</pre>
    </div>
    {{EmbedLiveSample("sampleMenuItemText",100,50,"","", "nobutton")}}</td>
   <td>Firefox</td>
   <td>Firefox 64 で削除</td>
  </tr>
  <tr>
   <td><code>menulist</code> {{Non-standard_Inline}}</td>
   <td>
    <div class="hidden" id="sampleMenuList">
    <pre class="brush: css">
div { color: black;
-moz-appearance: menulist;
-webkit-appearance: menulist; }</pre>

    <pre class="brush: html">
&lt;div&gt;Lorem&lt;/div&gt;</pre>
    </div>
    {{EmbedLiveSample("sampleMenuList",100,50,"","", "nobutton")}}</td>
   <td>Firefox Chrome Safari Edge</td>
   <td></td>
  </tr>
  <tr>
   <td><code>menulist-button</code> {{Non-standard_Inline}}</td>
   <td>
    <div class="hidden" id="sampleMenuListButton">
    <pre class="brush: css">
div { color: black;
-moz-appearance: menulist-button;
-webkit-appearance: menulist-button; }</pre>

    <pre class="brush: html">
&lt;div&gt;Lorem&lt;/div&gt;</pre>
    </div>
    {{EmbedLiveSample("sampleMenuListButton",100,50,"","", "nobutton")}}</td>
   <td>Firefox Chrome Safari Edge</td>
   <td>要素が開くことのできる menulist を示すボタンとしてスタイル付けられます。</td>
  </tr>
  <tr>
   <td><code>menulist-text</code> {{Non-standard_Inline}}</td>
   <td>
    <div class="hidden" id="sampleMenuListText">
    <pre class="brush: css">
div { color: black;
-moz-appearance: menulist-text;
-webkit-appearance: menulist-text; }</pre>

    <pre class="brush: html">
&lt;div&gt;Lorem&lt;/div&gt;</pre>
    </div>
    {{EmbedLiveSample("sampleMenuListText",100,50,"","", "nobutton")}}</td>
   <td>Firefox Chrome Safari Edge</td>
   <td></td>
  </tr>
  <tr>
   <td><code>menulist-textfield</code> {{Non-standard_Inline}}</td>
   <td>
    <div class="hidden" id="sampleMenuListTextfield">
    <pre class="brush: css">
div { color: black;
-moz-appearance: menulist-textfield;
-webkit-appearance: menulist-textfield; }</pre>

    <pre class="brush: html">
&lt;div&gt;Lorem&lt;/div&gt;</pre>
    </div>
    {{EmbedLiveSample("sampleMenuListTextfield",100,50,"","", "nobutton")}}</td>
   <td>Firefox Chrome Safari Edge</td>
   <td>要素が menulist のテキストフィールドとしてスタイル付けられます。 (Windows プラットフォームでは実装されていません)</td>
  </tr>
  <tr>
   <td><code>menupopup</code> {{Non-standard_Inline}}</td>
   <td>
    <div class="hidden" id="sampleMenuPopup">
    <pre class="brush: css">
div { color: black;
-moz-appearance: menupopup;
-webkit-appearance: menupopup; }</pre>

    <pre class="brush: html">
&lt;div&gt;Lorem&lt;/div&gt;</pre>
    </div>
    {{EmbedLiveSample("sampleMenuPopup",100,50,"","", "nobutton")}}</td>
   <td>Firefox</td>
   <td>Firefox 64 で削除</td>
  </tr>
  <tr>
   <td><code>menuradio</code> {{Non-standard_Inline}}</td>
   <td>
    <div class="hidden" id="sampleMenuRadio">
    <pre class="brush: css">
div { color: black;
-moz-appearance: menuradio;
-webkit-appearance: menuradio; }</pre>

    <pre class="brush: html">
&lt;div&gt;Lorem&lt;/div&gt;</pre>
    </div>
    {{EmbedLiveSample("sampleMenuRadio",100,50,"","", "nobutton")}}</td>
   <td>Firefox</td>
   <td>Firefox 64 で削除</td>
  </tr>
  <tr>
   <td><code>menuseparator</code> {{Non-standard_Inline}}</td>
   <td>
    <div class="hidden" id="sampleMenuSeparator">
    <pre class="brush: css">
div { color: transparent;
-moz-appearance: menuseparator;
-webkit-appearance: menuseparator; }</pre>

    <pre class="brush: html">
&lt;div&gt;Lorem&lt;/div&gt;</pre>
    </div>
    {{EmbedLiveSample("sampleMenuSeparator",100,50,"","", "nobutton")}}</td>
   <td>Firefox</td>
   <td>Firefox 64 で削除</td>
  </tr>
  <tr>
   <td><code>meter</code></td>
   <td>
    <div class="hidden" id="sampleMeter">
    <pre class="brush: css">
div{ color: black;
-webkit-appearance: meter; }</pre>

    <pre class="brush: html">
&lt;div&gt;Lorem&lt;/div&gt;</pre>
    </div>
    {{EmbedLiveSample("sampleMeter",100,50,"","", "nobutton")}}</td>
   <td>Chrome Safari Firefox</td>
   <td>Firefox 64 で追加</td>
  </tr>
  <tr>
   <td><code>meterbar</code> {{Non-standard_Inline}}</td>
   <td>
    <div class="hidden" id="sampleMeterbar">
    <pre class="brush: css">
div { color: black;
-moz-appearance: meterbar;
-webkit-appearance: meterbar; }</pre>

    <pre class="brush: html">
&lt;div&gt;Lorem&lt;/div&gt;</pre>
    </div>
    {{EmbedLiveSample("sampleMeterbar",100,50,"","", "nobutton")}}</td>
   <td>Firefox</td>
   <td>Firefox 16 の新機能。代わりに <code>meter</code> を使用のこと</td>
  </tr>
  <tr>
   <td><code>meterchunk</code> {{Non-standard_Inline}}</td>
   <td>
    <div class="hidden" id="sampleMeterchunk">
    <pre class="brush: css">
div { color: black;
-moz-appearance: meterchunk;
-webkit-appearance: meterchunk; }</pre>

    <pre class="brush: html">
&lt;div&gt;Lorem&lt;/div&gt;</pre>
    </div>
    {{EmbedLiveSample("sampleMeterchunk",100,50,"","", "nobutton")}}</td>
   <td>Firefox</td>
   <td>Firefox 16 で追加。 Firefox 64 で削除。</td>
  </tr>
  <tr>
   <td><code>number-input</code> {{Non-standard_Inline}}</td>
   <td>
    <div class="hidden" id="sampleNumberinput">
    <pre class="brush: css">
div { color: black;
-moz-appearance: number-input;
-webkit-appearance: number-input; }</pre>

    <pre class="brush: html">
&lt;div&gt;Lorem&lt;/div&gt;</pre>
    </div>
    {{EmbedLiveSample("sampleNumberInput",100,50,"","", "nobutton")}}</td>
   <td>Firefox</td>
   <td></td>
  </tr>
  <tr>
   <td><code>progress-bar</code></td>
   <td>
    <div class="hidden" id="sampleProgressBarWebkit">
    <pre class="brush: css">
div{ color: black;
-webkit-appearance: progress-bar; }</pre>

    <pre class="brush: html">
&lt;div&gt;Lorem&lt;/div&gt;</pre>
    </div>
    {{EmbedLiveSample("sampleProgressBarWebkit",100,50,"","", "nobutton")}}</td>
   <td>Chrome Safari Firefox</td>
   <td>Firefox 64 で追加</td>
  </tr>
  <tr>
   <td><code>progress-bar-value</code> {{Non-standard_Inline}}</td>
   <td>
    <div class="hidden" id="sampleProgressBarValueWebkit">
    <pre class="brush: css">
div{ color: black;
-webkit-appearance: progress-bar-value; }</pre>

    <pre class="brush: html">
&lt;div&gt;Lorem&lt;/div&gt;</pre>
    </div>
    {{EmbedLiveSample("sampleProgressBarValueWebkit",100,50,"","", "nobutton")}}</td>
   <td>Chrome Safari</td>
   <td></td>
  </tr>
  <tr>
   <td><code>progressbar</code> {{Non-standard_Inline}}</td>
   <td>
    <div class="hidden" id="sampleProgressBar">
    <pre class="brush: css">
div { color: black;
-moz-appearance: progressbar;
-webkit-appearance: progressbar; }</pre>

    <pre class="brush: html">
&lt;div&gt;Lorem&lt;/div&gt;</pre>
    </div>
    {{EmbedLiveSample("sampleProgressBar",100,50,"","", "nobutton")}}</td>
   <td>Firefox</td>
   <td>要素が進捗バーのようにスタイル付けられます。代わりに <code>progress-bar</code> を使用のこと</td>
  </tr>
  <tr>
   <td><code>progressbar-vertical</code> {{Non-standard_Inline}}</td>
   <td>
    <div class="hidden" id="sampleProgressBarVertical">
    <pre class="brush: css">
div { color: transparent;
-moz-appearance: progressbar-vertical;
-webkit-appearance: preogressbar-vertical; }</pre>

    <pre class="brush: html">
&lt;div&gt;Lorem&lt;/div&gt;</pre>
    </div>
    {{EmbedLiveSample("sampleProgressBarVertical",100,50,"","", "nobutton")}}</td>
   <td>Firefox</td>
   <td></td>
  </tr>
  <tr>
   <td><code>progresschunk</code> {{Non-standard_Inline}}</td>
   <td>
    <div class="hidden" id="sampleProgressChunk">
    <pre class="brush: css">
div { color: black;
-moz-appearance: progresschunk;
-webkit-appearance: progresschunk; }</pre>

    <pre class="brush: html">
&lt;div&gt;Lorem&lt;/div&gt;</pre>
    </div>
    {{EmbedLiveSample("sampleProgressChunk",100,50,"","", "nobutton")}}</td>
   <td>Firefox</td>
   <td>Firefox 64 で削除</td>
  </tr>
  <tr>
   <td><code>progresschunk-vertical</code> {{Non-standard_Inline}}</td>
   <td>
    <div class="hidden" id="sampleProgressChunkVertical">
    <pre class="brush: css">
div { color: black;
-moz-appearance: progresschunk-vertical;
-webkit-appearance: progresschunk-vertical; }</pre>

    <pre class="brush: html">
&lt;div&gt;Lorem&lt;/div&gt;</pre>
    </div>
    {{EmbedLiveSample("sampleProgressChunkVertical",100,50,"","", "nobutton")}}</td>
   <td>Firefox</td>
   <td>Firefox 64 で削除</td>
  </tr>
  <tr>
   <td><code>push-button</code> {{Non-standard_Inline}}</td>
   <td>
    <div class="hidden" id="samplePushButton">
    <pre class="brush: css">
div{ color: black; -webkit-appearance: push-button; }</pre>

    <pre class="brush: html">
&lt;div&gt;Lorem&lt;/div&gt;</pre>
    </div>
    {{EmbedLiveSample("samplePushButton",100,50,"","", "nobutton")}}</td>
   <td>Chrome Safari Edge</td>
   <td></td>
  </tr>
  <tr>
   <td><code>radio</code> {{Non-standard_Inline}}</td>
   <td>
    <div class="hidden" id="sampleRadio">
    <pre class="brush: css">
div { color: black;
-moz-appearance: radio;
-webkit-appearance: radio; }</pre>

    <pre class="brush: html">
&lt;div&gt;Lorem&lt;/div&gt;</pre>
    </div>
    {{EmbedLiveSample("sampleRadio",100,50,"","", "nobutton")}}</td>
   <td>Firefox Chrome Safari Edge</td>
   <td>要素がラジオボタンのように描画されます。実際の "radio button" 部分のみを含みます。</td>
  </tr>
  <tr>
   <td><code>radio-container</code> {{Non-standard_Inline}}</td>
   <td>
    <div class="hidden" id="sampleRadioContainer">
    <pre class="brush: css">
div { color: black;
-moz-appearance: radio-container;
-webkit-appearance: radio-container; }</pre>

    <pre class="brush: html">
&lt;div&gt;Lorem&lt;/div&gt;</pre>
    </div>
    {{EmbedLiveSample("sampleRadioContainer",100,50,"","", "nobutton")}}</td>
   <td>Firefox</td>
   <td>要素がラジオボタンのコンテナのように描画されます。あるプラットフォーム下では背景の発光効果を含みます。通常はラベルとラジオボタンを含みます。</td>
  </tr>
  <tr>
   <td><code>radio-label</code> {{Non-standard_Inline}}</td>
   <td>
    <div class="hidden" id="sampleRadioLabel">
    <pre class="brush: css">
div { color: black;
-moz-appearance: radio-label;
-webkit-appearance: radio-label; }</pre>

    <pre class="brush: html">
&lt;div&gt;Lorem&lt;/div&gt;</pre>
    </div>
    {{EmbedLiveSample("sampleRadioLabel",100,50,"","", "nobutton")}}</td>
   <td>Firefox</td>
   <td>Firefox 64 で削除</td>
  </tr>
  <tr>
   <td><code>radiomenuitem</code> {{Non-standard_Inline}}</td>
   <td>
    <div class="hidden" id="sampleRadioMenuItem">
    <pre class="brush: css">
div { color: black;
-moz-appearance: radiomenuitem;
-webkit-appearance: radiomenuitem; }</pre>

    <pre class="brush: html">
&lt;div&gt;Lorem&lt;/div&gt;</pre>
    </div>
    {{EmbedLiveSample("sampleRadioMenuItem",100,50,"","", "nobutton")}}</td>
   <td>Firefox</td>
   <td>Firefox 64 で削除</td>
  </tr>
  <tr>
   <td><code>range</code> {{Non-standard_Inline}}</td>
   <td>
    <div class="hidden" id="sampleRange">
    <pre class="brush: css">
div { color: black;
-moz-appearance: range;
-webkit-appearance: range; }</pre>
    range

    <pre class="brush: html">
&lt;div&gt;Lorem&lt;/div&gt;</pre>
    </div>
    {{EmbedLiveSample("sampleRange",100,50,"","", "nobutton")}}</td>
   <td>Firefox</td>
   <td></td>
  </tr>
  <tr>
   <td><code>range-thumb</code> {{Non-standard_Inline}}</td>
   <td>
    <div class="hidden" id="sampleRangeThumb">
    <pre class="brush: css">
div { color: black;
-moz-appearance: range-thumb;
-webkit-appearance: range-thumb; }</pre>

    <pre class="brush: html">
&lt;div&gt;Lorem&lt;/div&gt;</pre>
    </div>
    {{EmbedLiveSample("sampleRangeThumb",100,50,"","", "nobutton")}}</td>
   <td>Firefox</td>
   <td></td>
  </tr>
  <tr>
   <td><code>rating-level-indicator</code> {{Non-standard_Inline}}</td>
   <td>
    <div class="hidden" id="sample-rating-level-indicator">
    <pre class="brush: css">
div{ color: black;
-moz-appearance: rating-level-indicator;
-webkit-appearance: rating-level-indicator; }</pre>

    <pre class="brush: html">
&lt;div&gt;Lorem&lt;/div&gt;</pre>
    </div>
    {{EmbedLiveSample("sample-rating-level-indicator",100,50,"","","nobutton")}}</td>
   <td>Safari</td>
   <td></td>
  </tr>
  <tr>
   <td><code>resizer</code> {{Non-standard_Inline}}</td>
   <td>
    <div class="hidden" id="sampleResizer">
    <pre class="brush: css">
div { color: transparent;
-moz-appearance: resizer;
-webkit-appearance: resizer; }</pre>

    <pre class="brush: html">
&lt;div&gt;Lorem&lt;/div&gt;</pre>
    </div>
    {{EmbedLiveSample("sampleResizer",100,50,"","", "nobutton")}}</td>
   <td>Firefox</td>
   <td>Firefox 63 で削除</td>
  </tr>
  <tr>
   <td><code>resizerpanel</code> {{Non-standard_Inline}}</td>
   <td>
    <div class="hidden" id="sampleResizerPanel">
    <pre class="brush: css">
div { color: black;
-moz-appearance: resizerpanel;
-webkit-appearance: resizerpanel; }</pre>

    <pre class="brush: html">
&lt;div&gt;Lorem&lt;/div&gt;</pre>
    </div>
    {{EmbedLiveSample("sampleResizerPanel",100,50,"","", "nobutton")}}</td>
   <td>Firefox</td>
   <td>Firefox 63 で削除</td>
  </tr>
  <tr>
   <td><code>scale-horizontal</code> {{Non-standard_Inline}}</td>
   <td>
    <div class="hidden" id="sampleScaleHorizontal">
    <pre class="brush: css">
div { color: transparent;
-moz-appearance: scale-horizontal;
-webkit-appearance: scale-horizontal; }</pre>

    <pre class="brush: html">
&lt;div&gt;Lorem&lt;/div&gt;</pre>
    </div>
    {{EmbedLiveSample("sampleScaleHorizontal",100,50,"","", "nobutton")}}</td>
   <td>Firefox</td>
   <td></td>
  </tr>
  <tr>
   <td><code>scalethumbend</code> {{Non-standard_Inline}}</td>
   <td>
    <div class="hidden" id="sampleThumbEnd">
    <pre class="brush: css">
div { color: black;
-moz-appearance: scalethumbend;
-webkit-appearance: scalethumbend; }</pre>

    <pre class="brush: html">
&lt;div&gt;Lorem&lt;/div&gt;</pre>
    </div>
    {{EmbedLiveSample("sampleThumbEnd",100,50,"","", "nobutton")}}</td>
   <td>Firefox</td>
   <td></td>
  </tr>
  <tr>
   <td><code>scalethumb-horizontal</code> {{Non-standard_Inline}}</td>
   <td>
    <div class="hidden" id="sampleScaleThumbHorizontal">
    <pre class="brush: css">
div { color: transparent;
-moz-appearance: scalethumb-horizontal;
-webkit-appearance: scalethumb-horizontal; }</pre>

    <pre class="brush: html">
&lt;div&gt;Lorem&lt;/div&gt;</pre>
    </div>
    {{EmbedLiveSample("sampleScaleThumbHorizontal",100,50,"","", "nobutton")}}</td>
   <td>Firefox</td>
   <td></td>
  </tr>
  <tr>
   <td><code>scalethumbstart</code> {{Non-standard_Inline}}</td>
   <td>
    <div class="hidden" id="sampleScaleThumbStart">
    <pre class="brush: css">
div { color: black;
-moz-appearance: scalethumbstart;
-webkit-appearance: scalethumbstart; }</pre>

    <pre class="brush: html">
&lt;div&gt;Lorem&lt;/div&gt;</pre>
    </div>
    {{EmbedLiveSample("sampleScaleThumbStart",100,50,"","", "nobutton")}}</td>
   <td>Firefox</td>
   <td></td>
  </tr>
  <tr>
   <td><code>scalethumbtick</code> {{Non-standard_Inline}}</td>
   <td>
    <div class="hidden" id="sampleScaleThumbTick">
    <pre class="brush: css">
div { color: black;
-moz-appearance: scalethumbtick;
-webkit-appearance: scalethumbtick; }</pre>

    <pre class="brush: html">
&lt;div&gt;Lorem&lt;/div&gt;</pre>
    </div>
    {{EmbedLiveSample("sampleScaleThumbTick",100,50,"","", "nobutton")}}</td>
   <td>Firefox</td>
   <td></td>
  </tr>
  <tr>
   <td><code>scalethumb-vertical</code> {{Non-standard_Inline}}</td>
   <td>
    <div class="hidden" id="sampleScaleThumbVertical">
    <pre class="brush: css">
div { color: black;
-moz-appearance: scalethumb-vertical;
-webkit-appearance: scalethumb-vertical; }</pre>

    <pre class="brush: html">
&lt;div&gt;Lorem&lt;/div&gt;</pre>
    </div>
    {{EmbedLiveSample("sampleScaleThumbVertical",100,50,"","", "nobutton")}}</td>
   <td>Firefox</td>
   <td></td>
  </tr>
  <tr>
   <td><code>scale-vertical</code> {{Non-standard_Inline}}</td>
   <td>
    <div class="hidden" id="sampleScaleVertical">
    <pre class="brush: css">
div { color: transparent;
-moz-appearance: scale-vertical;
-webkit-appearance: scale-vertical; }</pre>

    <pre class="brush: html">
&lt;div&gt;Lorem&lt;/div&gt;</pre>
    </div>
    {{EmbedLiveSample("sampleScaleVertical",100,50,"","", "nobutton")}}</td>
   <td>Firefox</td>
   <td></td>
  </tr>
  <tr>
   <td><code>scrollbarbutton-down</code> {{Non-standard_Inline}}</td>
   <td>
    <div class="hidden" id="sampleScrollbarButtonDown">
    <pre class="brush: css">
div { color: black;
-moz-appearance: scrollbarbutton-down;
-webkit-appearance: scrollbarbutton-down; }</pre>

    <pre class="bruh: html">
&lt;div&gt;Lorem&lt;/div&gt;</pre>
    </div>
    {{EmbedLiveSample("sampleScrollbarButtonDown",100,50,"","", "nobutton")}}</td>
   <td>Firefox</td>
   <td>Firefox 63 で削除</td>
  </tr>
  <tr>
   <td><code>scrollbarbutton-left</code> {{Non-standard_Inline}}</td>
   <td>
    <div class="hidden" id="sampleScrollbarButtonLeft">
    <pre class="brush: css">
div { color: black;
-moz-appearance: scrollbarbutton-left;
-webkit-appearance: scrollbarbutton-left; }</pre>

    <pre class="bruh: html">
&lt;div&gt;Lorem&lt;/div&gt;</pre>
    </div>
    {{EmbedLiveSample("sampleScrollbarButtonLeft",100,50,"","", "nobutton")}}</td>
   <td>Firefox</td>
   <td>Firefox 63 で削除</td>
  </tr>
  <tr>
   <td><code>scrollbarbutton-right</code> {{Non-standard_Inline}}</td>
   <td>
    <div class="hidden" id="sampleScrollbarButtonRight">
    <pre class="brush: css">
div { color: black;
-moz-appearance: scrollbarbutton-right;
-webkit-appearance: scrollbarbutton-right; }</pre>

    <pre class="bruh: html">
&lt;div&gt;Lorem&lt;/div&gt;</pre>
    </div>
    {{EmbedLiveSample("sampleScrollbarButtonRight",100,50,"","", "nobutton")}}</td>
   <td>Firefox</td>
   <td>Firefox 63 で削除</td>
  </tr>
  <tr>
   <td><code>scrollbarbutton-up</code> {{Non-standard_Inline}}</td>
   <td>
    <div class="hidden" id="sampleScrollbarButtonUp">
    <pre class="brush: css">
div { color: black;
-moz-appearance: scrollbarbutton-up;
-webkit-appearance: scrollbarbutton-up; }</pre>

    <pre class="bruh: html">
&lt;div&gt;Lorem&lt;/div&gt;</pre>
    </div>
    {{EmbedLiveSample("sampleScrollbarButtonUp",100,50,"","", "nobutton")}}</td>
   <td>Firefox</td>
   <td>Firefox 63 で削除</td>
  </tr>
  <tr>
   <td><code>scrollbarthumb-horizontal</code> {{Non-standard_Inline}}</td>
   <td>
    <div class="hidden" id="sampleScrollbarThumbHorizontal">
    <pre class="brush: css">
div { color: black;
-moz-appearance: scrollbarthumb-horizontal;
-webkit-appearance: scrollbarthumb-horizontal; }</pre>

    <pre class="bruh: html">
&lt;div&gt;Lorem&lt;/div&gt;</pre>
    </div>
    {{EmbedLiveSample("sampleScrollbarThumbHorizontal",100,50,"","", "nobutton")}}</td>
   <td>Firefox</td>
   <td></td>
  </tr>
  <tr>
   <td><code>scrollbarthumb-vertical</code> {{Non-standard_Inline}}</td>
   <td>
    <div class="hidden" id="sampleScrollbarThumbVertical">
    <pre class="brush: css">
div { color: black;
-moz-appearance: scrollbarthumb-vertical;
-webkit-appearance: scrollbarthumb-vertical; }</pre>

    <pre class="bruh: html">
&lt;div&gt;Lorem&lt;/div&gt;</pre>
    </div>
    {{EmbedLiveSample("sampleScrollbarThumbVertical",100,50,"","", "nobutton")}}</td>
   <td>Firefox</td>
   <td></td>
  </tr>
  <tr>
   <td><code>scrollbartrack-horizontal</code> {{Non-standard_Inline}}</td>
   <td>
    <div class="hidden" id="sampleScrollbarTrackHorizontal">
    <pre class="brush: css">
div { color: black;
-moz-appearance: scrollbartrack-horizontal;
-webkit-appearance: scrollbartrack-horizontal; }</pre>

    <pre class="bruh: html">
&lt;div&gt;Lorem&lt;/div&gt;</pre>
    </div>
    {{EmbedLiveSample("sampleScrollbarTrackHorizontal",100,50,"","", "nobutton")}}</td>
   <td>Firefox</td>
   <td></td>
  </tr>
  <tr>
   <td><code>scrollbartrack-vertical</code> {{Non-standard_Inline}}</td>
   <td>
    <div class="hidden" id="sampleScrollbarTrackVertical">
    <pre class="brush: css">
div { color: black;
-moz-appearance: scrollbartrack-vertical;
-webkit-appearance: scrollbarbartrack-vertical; }</pre>

    <pre class="bruh: html">
&lt;div&gt;Lorem&lt;/div&gt;</pre>
    </div>
    {{EmbedLiveSample("sampleScrollbarTrackVertical",100,50,"","", "nobutton")}}</td>
   <td>Firefox</td>
   <td></td>
  </tr>
  <tr>
   <td><code>searchfield</code> {{Non-standard_Inline}}</td>
   <td>
    <div class="hidden" id="sampleSearchField">
    <pre class="brush: css">
div { color: black;
-moz-appearance: searchfield;
-webkit-appearance: searchfield; }</pre>

    <pre class="bruh: html">
&lt;div&gt;Lorem&lt;/div&gt;</pre>
    </div>
    {{EmbedLiveSample("sampleSearchField",100,50,"","", "nobutton")}}</td>
   <td>Firefox Chrome Safari Edge</td>
   <td></td>
  </tr>
  <tr>
   <td><code>searchfield-decoration</code> {{Non-standard_Inline}}</td>
   <td>
    <div class="hidden" id="sample-searchfield-decoration">
    <pre class="brush: css">
div{ color: black;
-moz-appearance: searchfield-decoration;
-webkit-appearance: searchfield-decoration; }</pre>

    <pre class="brush: html">
&lt;div&gt;Lorem&lt;/div&gt;</pre>
    </div>
    {{EmbedLiveSample("sample-searchfield-decoration",100,50,"","","nobutton")}}</td>
   <td>Safari Edge</td>
   <td></td>
  </tr>
  <tr>
   <td><code>searchfield-results-decoration</code> {{Non-standard_Inline}}</td>
   <td>
    <div class="hidden" id="sample-searchfield-results-decoration">
    <pre class="brush: css">
div{ color: black;
-moz-appearance: searchfield-results-decoration;
-webkit-appearance: searchfield-results-decoration; }</pre>

    <pre class="brush: html">
&lt;div&gt;Lorem&lt;/div&gt;</pre>
    </div>
    {{EmbedLiveSample("sample-searchfield-results-decoration",100,50,"","","nobutton")}}</td>
   <td>Safari Edge</td>
   <td></td>
  </tr>
  <tr>
   <td><code>searchfield-results-button</code> {{Non-standard_Inline}}</td>
   <td>
    <div class="hidden" id="sample-searchfield-results-button">
    <pre class="brush: css">
div{ color: black;
-moz-appearance: searchfield-results-button;
-webkit-appearance: searchfield-results-button; }</pre>

    <pre class="brush: html">
&lt;div&gt;Lorem&lt;/div&gt;</pre>
    </div>
    {{EmbedLiveSample("sample-searchfield-results-button",100,50,"","","nobutton")}}</td>
   <td>Safari Edge</td>
   <td></td>
  </tr>
  <tr>
   <td><code>searchfield-cancel-button</code> {{Non-standard_Inline}}</td>
   <td>
    <div class="hidden" id="sampleSearchFieldCancelButton">
    <pre class="brush: css">
div{ color: black;
-webkit-appearance: searchfield-cancel-button; }</pre>

    <pre class="brush: html">
&lt;div&gt;Lorem&lt;/div&gt;</pre>
    </div>
    {{EmbedLiveSample("sampleSearchFieldCancelButton",100,50,"","", "nobutton")}}</td>
   <td>Chrome Safari Edge</td>
   <td></td>
  </tr>
  <tr>
   <td><code>snapshotted-plugin-overlay</code> {{Non-standard_Inline}}</td>
   <td>
    <div class="hidden" id="sample-snapshotted-plugin-overlay">
    <pre class="brush: css">
div{ color: black;
-moz-appearance: snapshotted-plugin-overlay;
-webkit-appearance: snapshotted-plugin-overlay; }</pre>

    <pre class="brush: html">
&lt;div&gt;Lorem&lt;/div&gt;</pre>
    </div>
    {{EmbedLiveSample("sample-snapshotted-plugin-overlay",100,50,"","","nobutton")}}</td>
   <td>Safari</td>
   <td></td>
  </tr>
  <tr>
   <td><code>separator</code> {{Non-standard_Inline}}</td>
   <td>
    <div class="hidden" id="sampleSeparator">
    <pre class="brush: css">
div { color: transparent;
-moz-appearance: separator;
-webkit-appearance: separator; }</pre>

    <pre class="bruh: html">
&lt;div&gt;Lorem&lt;/div&gt;</pre>
    </div>
    {{EmbedLiveSample("sampleSeparator",100,50,"","", "nobutton")}}</td>
   <td>Firefox</td>
   <td>Firefox 64 で削除</td>
  </tr>
  <tr>
   <td><code>sheet</code> {{Non-standard_Inline}}</td>
   <td>
    <div class="hidden" id="sampleSheet">
    <pre class="brush: css">
div { color: black;
-moz-appearance: sheet;
-webkit-appearance: sheet; }</pre>

    <pre class="brush: html">
&lt;div&gt;Lorem&lt;/div&gt;</pre>
    </div>
    {{EmbedLiveSample("sampleSheet",100,50,"","", "nobutton")}}</td>
   <td>None</td>
   <td></td>
  </tr>
  <tr>
   <td><code>slider-horizontal</code> {{Non-standard_Inline}}</td>
   <td>
    <div class="hidden" id="sampleSliderHorizontal">
    <pre class="brush: css">
div{ color: black;
-webkit-appearance: slider-horizontal; }</pre>

    <pre class="brush: html">
&lt;div&gt;Lorem&lt;/div&gt;</pre>
    </div>
    {{EmbedLiveSample("sampleSliderHorizontal",100,50,"","", "nobutton")}}</td>
   <td>Chrome Safari Edge</td>
   <td></td>
  </tr>
  <tr>
   <td><code>slider-vertical</code> {{Non-standard_Inline}}</td>
   <td>
    <div class="hidden" id="sampleSliderVertical">
    <pre class="brush: css">
div{ color: black;
-webkit-appearance: slider-vertical; }</pre>

    <pre class="brush: html">
&lt;div&gt;Lorem&lt;/div&gt;</pre>
    </div>
    {{EmbedLiveSample("sampleSliderVertical",100,50,"","", "nobutton")}}</td>
   <td>Chrome Safari Edge</td>
   <td></td>
  </tr>
  <tr>
   <td><code>sliderthumb-horizontal</code> {{Non-standard_Inline}}</td>
   <td>
    <div class="hidden" id="sampleSliderThumbHorizontal">
    <pre class="brush: css">
div{ color: black;
-webkit-appearance: slider-thumb-horizontal; }</pre>

    <pre class="brush: html">
&lt;div&gt;Lorem&lt;/div&gt;</pre>
    </div>
    {{EmbedLiveSample("sampleSliderThumbHorizontal",100,50,"","", "nobutton")}}</td>
   <td>Chrome Safari Edge</td>
   <td></td>
  </tr>
  <tr>
   <td><code>sliderthumb-vertical</code> {{Non-standard_Inline}}</td>
   <td>
    <div class="hidden" id="sampleSliderThumbVertical">
    <pre class="brush: css">
div{ color: black;
-webkit-appearance: slider-thumb-vertical; }</pre>

    <pre class="brush: html">
&lt;div&gt;Lorem&lt;/div&gt;</pre>
    </div>
    {{EmbedLiveSample("sampleSliderThumbVertical",100,50,"","", "nobutton")}}</td>
   <td>Chrome Safari Edge</td>
   <td></td>
  </tr>
  <tr>
   <td><code>spinner</code> {{Non-standard_Inline}}</td>
   <td>
    <div class="hidden" id="sampleSpinner">
    <pre class="brush: css">
div { color: transparent;
-moz-appearance: spinner;
-webkit-appearance: spinner; }</pre>

    <pre class="brush: html">
&lt;div&gt;Lorem&lt;/div&gt;</pre>
    </div>
    {{EmbedLiveSample("sampleSpinner",100,50,"","", "nobutton")}}</td>
   <td>Firefox</td>
   <td>Firefox 64 で削除</td>
  </tr>
  <tr>
   <td><code>spinner-downbutton</code> {{Non-standard_Inline}}</td>
   <td>
    <div class="hidden" id="sampleSpinnerDownbutton">
    <pre class="brush: css">
div { color: black;
-moz-appearance: spinner-downbutton;
-webkit-appearance: spinner-downbutton; }</pre>

    <pre class="brush: html">
&lt;div&gt;Lorem&lt;/div&gt;</pre>
    </div>
    {{EmbedLiveSample("sampleSpinnerDownbutton",100,50,"","", "nobutton")}}</td>
   <td>Firefox</td>
   <td>Firefox 64 で削除</td>
  </tr>
  <tr>
   <td><code>spinner-textfield</code> {{Non-standard_Inline}}</td>
   <td>
    <div class="hidden" id="sampleSpinnerTextfield">
    <pre class="brush: css">
div { color: black;
-moz-appearance: spinner-textfield;
-webkit-appearance: spinner-textfield; }</pre>

    <pre class="brush: html">
&lt;div&gt;Lorem&lt;/div&gt;</pre>
    </div>
    {{EmbedLiveSample("sampleSpinnerTextfield",100,50,"","", "nobutton")}}</td>
   <td>Firefox</td>
   <td>Firefox 64 で削除</td>
  </tr>
  <tr>
   <td><code>spinner-upbutton</code> {{Non-standard_Inline}}</td>
   <td>
    <div class="hidden" id="sampleSpinnerUpbutton">
    <pre class="brush: css">
div { color: black;
-moz-appearance: spinner-upbutton;
-webkit-appearance: spinner-upbutton; }</pre>

    <pre class="brush: html">
&lt;div&gt;Lorem&lt;/div&gt;</pre>
    </div>
    {{EmbedLiveSample("sampleSpinnerUpbutton",100,50,"","", "nobutton")}}</td>
   <td>Firefox</td>
   <td>Firefox 64 で削除</td>
  </tr>
  <tr>
   <td><code>splitter</code> {{Non-standard_Inline}}</td>
   <td>
    <div class="hidden" id="sampleSplitter">
    <pre class="brush: css">
div { color: transparent;
-moz-appearance: splitter;
-webkit-appearance: splitter; }</pre>

    <pre class="brush: html">
&lt;div&gt;Lorem&lt;/div&gt;</pre>
    </div>
    {{EmbedLiveSample("sampleSplitter",100,50,"","", "nobutton")}}</td>
   <td>Firefox</td>
   <td>Firefox 64 で削除</td>
  </tr>
  <tr>
   <td><code>square-button</code> {{Non-standard_Inline}}</td>
   <td>
    <div class="hidden" id="sampleSquareButton">
    <pre class="brush: css">
div{ color: black;
-moz-appearance: square-button;
-webkit-appearance: square-button; }</pre>

    <pre class="brush: html">
&lt;div&gt;Lorem&lt;/div&gt;</pre>
    </div>
    {{EmbedLiveSample("sampleSquareButton",100,50,"","", "nobutton")}}</td>
   <td>Chrome Safari Edge</td>
   <td></td>
  </tr>
  <tr>
   <td><code>statusbar</code> {{Non-standard_Inline}}</td>
   <td>
    <div class="hidden" id="sampleStatusBar">
    <pre class="brush: css">
div { color: black;
-moz-appearance: statusbar;
-webkit-appearance: statusbar; }</pre>

    <pre class="brush: html">
&lt;div&gt;Lorem&lt;/div&gt;</pre>
    </div>
    {{EmbedLiveSample("sampleStatusBar",100,50,"","", "nobutton")}}</td>
   <td>Firefox</td>
   <td>Firefox 64 で削除</td>
  </tr>
  <tr>
   <td><code>statusbarpanel</code> {{Non-standard_Inline}}</td>
   <td>
    <div class="hidden" id="sampleStatusBarPanel">
    <pre class="brush: css">
div { color: black;
-moz-appearance: statusbarpanel;
-webkit-appearance: statusbarpanel; }</pre>

    <pre class="brush: html">
&lt;div&gt;Lorem&lt;/div&gt;</pre>
    </div>
    {{EmbedLiveSample("sampleStatusBarPanel",100,50,"","", "nobutton")}}</td>
   <td>Firefox</td>
   <td>Firefox 64 で削除</td>
  </tr>
  <tr>
   <td><code>tab</code> {{Non-standard_Inline}}</td>
   <td>
    <div class="hidden" id="sampleTab">
    <pre class="brush: css">
div { color: black; height: 20px;
-moz-appearance: tab;
-webkit-appearance: tab; }</pre>

    <pre class="brush: html">
&lt;div&gt;Lorem&lt;/div&gt;</pre>
    </div>
    {{EmbedLiveSample("sampleTab",100,50,"","", "nobutton")}}</td>
   <td>Firefox</td>
   <td>Firefox 64 で削除</td>
  </tr>
  <tr>
   <td><code>tabpanel</code> {{Non-standard_Inline}}</td>
   <td>
    <div class="hidden" id="sampleTabPanel">
    <pre class="brush: css">
div { color: black;
-moz-appearance: tabpanel;
-webkit-appearance: tabpanel; }</pre>

    <pre class="brush: html">
&lt;div&gt;Lorem&lt;/div&gt;</pre>
    </div>
    {{EmbedLiveSample("sampleTabPanel",100,50,"","", "nobutton")}}</td>
   <td>Firefox</td>
   <td>Firefox 64 で削除</td>
  </tr>
  <tr>
   <td><code>tabpanels</code> {{Non-standard_Inline}}</td>
   <td>
    <div class="hidden" id="sampleTabPanels">
    <pre class="brush: css">
div { color: black;
-moz-appearance: tabpanels;
-webkit-appearance: tabpanels; }</pre>

    <pre class="brush: html">
&lt;div&gt;Lorem&lt;/div&gt;</pre>
    </div>
    {{EmbedLiveSample("sampleTabPanels",100,50,"","", "nobutton")}}</td>
   <td>Firefox</td>
   <td>Firefox 64 で削除</td>
  </tr>
  <tr>
   <td><code>tab-scroll-arrow-back</code> {{Non-standard_Inline}}</td>
   <td>
    <div class="hidden" id="sampleTabScrollArrowBack">
    <pre class="brush: css">
div { color: black;
-moz-appearance: tab-scroll-arrow-back;
-webkit-appearance: tab-scroll-arrow-back; }</pre>

    <pre class="brush: html">
&lt;div&gt;Lorem&lt;/div&gt;</pre>
    </div>
    {{EmbedLiveSample("sampleTabScrollArrowBack",100,50,"","", "nobutton")}}</td>
   <td>Firefox</td>
   <td>Firefox 64 で削除</td>
  </tr>
  <tr>
   <td><code>tab-scroll-arrow-forward</code> {{Non-standard_Inline}}</td>
   <td>
    <div class="hidden" id="sampleTabScrollArrowForward">
    <pre class="brush: css">
div { color: black;
-moz-appearance: tab-scroll-arrow-forward;
-webkit-appearance: tab-scroll-arrow-forward; }</pre>

    <pre class="brush: html">
&lt;div&gt;Lorem&lt;/div&gt;</pre>
    </div>
    {{EmbedLiveSample("sampleTabScrollArrowForward",100,50,"","", "nobutton")}}</td>
   <td>Firefox</td>
   <td>Firefox 64 で削除</td>
  </tr>
  <tr>
   <td><code>textarea</code></td>
   <td>
    <div class="hidden" id="sampleTextArea">
    <pre class="brush: css">
div{ color: black;
-webkit-appearance: textarea; }</pre>

    <pre class="brush: html">
&lt;div&gt;Lorem&lt;/div&gt;</pre>
    </div>
    {{EmbedLiveSample("sampleTextArea",100,50,"","", "nobutton")}}</td>
   <td>Firefox Chrome Safari Edge</td>
   <td></td>
  </tr>
  <tr>
   <td><code>textfield</code> {{Non-standard_Inline}}</td>
   <td>
    <div class="hidden" id="sampleTextField">
    <pre class="brush: css">
div { color: black;
-moz-appearance: textfield;
-webkit-appearance: textfield; }</pre>

    <pre class="brush: html">
&lt;div&gt;Lorem&lt;/div&gt;</pre>
    </div>
    {{EmbedLiveSample("sampleTextField",100,50,"","", "nobutton")}}</td>
   <td>Firefox Chrome Safari Edge</td>
   <td></td>
  </tr>
  <tr>
   <td><code>textfield-multiline</code> {{Non-standard_Inline}}</td>
   <td>
    <div class="hidden" id="sampleTextfieldMultiline">
    <pre class="brush: css">
div { color: black;
-moz-appearance: textfield-multiline;
-webkit-appearance: textfield-multiline; }</pre>

    <pre class="brush: html">
&lt;div&gt;Lorem&lt;/div&gt;</pre>
    </div>
    {{EmbedLiveSample("sampleTextfieldMultiline",100,50,"","", "nobutton")}}</td>
   <td>Firefox</td>
   <td>代わりに <code>textarea</code> を使用のこと</td>
  </tr>
  <tr>
   <td><code>toolbar</code> {{Non-standard_Inline}}</td>
   <td>
    <div class="hidden" id="sampleToolbar">
    <pre class="brush: css">
div { color: black;
-moz-appearance: toolbar;
-webkit-appearance: toolbar; }</pre>

    <pre class="brush: html">
&lt;div&gt;Lorem&lt;/div&gt;</pre>
    </div>
    {{EmbedLiveSample("sampleToolbar",100,50,"","", "nobutton")}}</td>
   <td>Firefox</td>
   <td>Firefox 64 で削除</td>
  </tr>
  <tr>
   <td><code>toolbarbutton</code> {{Non-standard_Inline}}</td>
   <td>
    <div class="hidden" id="sampleToolbarButton">
    <pre class="brush: css">
div { color: black;
-moz-appearance: toolbarbutton;
-webkit-appearance: toolbarbutton; }</pre>

    <pre class="brush: html">
&lt;div&gt;Lorem&lt;/div&gt;</pre>
    </div>
    {{EmbedLiveSample("sampleToolbarButton",100,50,"","", "nobutton")}}</td>
   <td>Firefox</td>
   <td>Firefox 64 で削除</td>
  </tr>
  <tr>
   <td><code>toolbarbutton-dropdown</code> {{Non-standard_Inline}}</td>
   <td>
    <div class="hidden" id="sampleToolbarButtonDropdown">
    <pre class="brush: css">
div { color: black;
-moz-appearance: toolbarbutton-dropdown;
-webkit-appearance: toolbarbutton-dropdown; }</pre>

    <pre class="brush: html">
&lt;div&gt;Lorem&lt;/div&gt;</pre>
    </div>
    {{EmbedLiveSample("sampleToolbarButtonDropdown",100,50,"","", "nobutton")}}</td>
   <td>Firefox</td>
   <td>Firefox 64 で削除</td>
  </tr>
  <tr>
   <td><code>toolbargripper</code> {{Non-standard_Inline}}</td>
   <td>
    <div class="hidden" id="sampleToolbarGripper">
    <pre class="brush: css">
div { color: black;
-moz-appearance: toolbargripper;
-webkit-appearance: toolbargripper; }</pre>

    <pre class="brush: html">
&lt;div&gt;Lorem&lt;/div&gt;</pre>
    </div>
    {{EmbedLiveSample("sampleToolbarGripper",100,50,"","", "nobutton")}}</td>
   <td>Firefox</td>
   <td>Firefox 64 で削除</td>
  </tr>
  <tr>
   <td><code>toolbox</code> {{Non-standard_Inline}}</td>
   <td>
    <div class="hidden" id="sampleToolbox">
    <pre class="brush: css">
div { color: black;
-moz-appearance: toolbox;
-webkit-appearance: toolbox; }</pre>

    <pre class="brush: html">
&lt;div&gt;Lorem&lt;/div&gt;</pre>
    </div>
    {{EmbedLiveSample("sampleToolbox",100,50,"","", "nobutton")}}</td>
   <td>Firefox</td>
   <td>Firefox 64 で削除</td>
  </tr>
  <tr>
   <td><code>tooltip</code> {{Non-standard_Inline}}</td>
   <td>
    <div class="hidden" id="sampleTooltip">
    <pre class="brush: css">
div { color: black;
-moz-appearance: tooltip;
-webkit-appearance: tooltip; }</pre>

    <pre class="brush: html">
&lt;div&gt;Lorem&lt;/div&gt;</pre>
    </div>
    {{EmbedLiveSample("sampleTooltip",100,50,"","", "nobutton")}}</td>
   <td>Firefox</td>
   <td>Firefox 64 で削除</td>
  </tr>
  <tr>
   <td><code>treeheader</code> {{Non-standard_Inline}}</td>
   <td>
    <div class="hidden" id="sampleTreeHeader">
    <pre class="brush: css">
div { color: black;
-moz-appearance: treeheader;
-webkit-appearance: treeheader; }</pre>

    <pre class="brush: html">
&lt;div&gt;Lorem&lt;/div&gt;</pre>
    </div>
    {{EmbedLiveSample("sampleTreeHeader",100,50,"","", "nobutton")}}</td>
   <td>Firefox</td>
   <td>Firefox 64 で削除</td>
  </tr>
  <tr>
   <td><code>treeheadercell</code> {{Non-standard_Inline}}</td>
   <td>
    <div class="hidden" id="sampleTreeHeaderCell">
    <pre class="brush: css">
div { color: black; height:20px;
-moz-appearance: treeheadercell;
-webkit-appearance: treeheadercell; }</pre>

    <pre class="brush: html">
&lt;div&gt;Lorem&lt;/div&gt;</pre>
    </div>
    {{EmbedLiveSample("sampleTreeHeaderCell",100,50,"","", "nobutton")}}</td>
   <td>Firefox</td>
   <td>Firefox 64 で削除</td>
  </tr>
  <tr>
   <td><code>treeheadersortarrow</code> {{Non-standard_Inline}}</td>
   <td>
    <div class="hidden" id="sampleTreeHeaderSortArrow">
    <pre class="brush: css">
div { color: black;
-moz-appearance: treeheadersortarrow;
-webkit-appearance: treeheadersortarrow; }</pre>

    <pre class="brush: html">
&lt;div&gt;Lorem&lt;/div&gt;</pre>
    </div>
    {{EmbedLiveSample("sampleTreeHeaderSortArrow",100,50,"","", "nobutton")}}</td>
   <td>Firefox</td>
   <td>Firefox 64 で削除</td>
  </tr>
  <tr>
   <td><code>treeitem</code> {{Non-standard_Inline}}</td>
   <td>
    <div class="hidden" id="sampleTreeItem">
    <pre class="brush: css">
div { color: black;
-moz-appearance: treeitem;
-webkit-appearance: treeitem; }</pre>

    <pre class="brush: html">
&lt;div&gt;Lorem&lt;/div&gt;</pre>
    </div>
    {{EmbedLiveSample("sampleTreeItem",100,50,"","", "nobutton")}}</td>
   <td>Firefox</td>
   <td>Firefox 64 で削除</td>
  </tr>
  <tr>
   <td><code>treeline</code> {{Non-standard_Inline}}</td>
   <td>
    <div class="hidden" id="sampleTreeLine">
    <pre class="brush: css">
div { color: black;
-moz-appearance: treeline;
-webkit-appearance: treeline; }</pre>

    <pre class="brush: html">
&lt;div&gt;Lorem&lt;/div&gt;</pre>
    </div>
    {{EmbedLiveSample("sampleTreeLine",100,50,"","", "nobutton")}}</td>
   <td>Firefox</td>
   <td>Firefox 64 で削除</td>
  </tr>
  <tr>
   <td><code>treetwisty</code> {{Non-standard_Inline}}</td>
   <td>
    <div class="hidden" id="sampleTreeTwisty">
    <pre class="brush: css">
div { color: transparent;
-moz-appearance: treetwisty;
-webkit-appearance: treetwisty; }</pre>

    <pre class="brush: html">
&lt;div&gt;Lorem&lt;/div&gt;</pre>
    </div>
    {{EmbedLiveSample("sampleTreeTwisty",100,50,"","", "nobutton")}}</td>
   <td>Firefox</td>
   <td>Firefox 64 で削除</td>
  </tr>
  <tr>
   <td><code>treetwistyopen</code> {{Non-standard_Inline}}</td>
   <td>
    <div class="hidden" id="sampleTreeTwistyOpen">
    <pre class="brush: css">
div { color: transparent;
-moz-appearance: treetwistyopen;
-webkit-appearance: treetwistyopen; }</pre>

    <pre class="brush: html">
&lt;div&gt;Lorem&lt;/div&gt;</pre>
    </div>
    {{EmbedLiveSample("sampleTreeTwistyOpen",100,50,"","", "nobutton")}}</td>
   <td>Firefox</td>
   <td>Firefox 64 で削除</td>
  </tr>
  <tr>
   <td><code>treeview</code> {{Non-standard_Inline}}</td>
   <td>
    <div class="hidden" id="sampleTreeView">
    <pre class="brush: css">
div { color: black;
-moz-appearance: treeview;
-webkit-appearance: treeview; }</pre>

    <pre class="brush: html">
&lt;div&gt;Lorem&lt;/div&gt;</pre>
    </div>
    {{EmbedLiveSample("sampleTreeView",100,50,"","", "nobutton")}}</td>
   <td>Firefox</td>
   <td>Firefox 64 で削除</td>
  </tr>
  <tr>
   <td><code>relevancy-level-indicator</code> {{Non-standard_Inline}}</td>
   <td>
    <div class="hidden" id="sample-relevancy-level-indicator">
    <pre class="brush: css">
div{ color: black;
-moz-appearance: relevancy-level-indicator;
-webkit-appearance: relevancy-level-indicator; }</pre>

    <pre class="brush: html">
&lt;div&gt;Lorem&lt;/div&gt;</pre>
    </div>
    {{EmbedLiveSample("sample-relevancy-level-indicator",100,50,"","","nobutton")}}</td>
   <td>Safari</td>
   <td></td>
  </tr>
  <tr>
   <td><code>-moz-win-borderless-glass</code> {{Non-standard_Inline}}{{Gecko_MinVersion_Inline("2.0")}}</td>
   <td>
    <div class="hidden" id="sampleWinBorderlessGlass">
    <pre class="brush: css">
div { color: black;
-moz-appearance: -moz-win-borderless-glass; }</pre>

    <pre class="brush: html">
&lt;div&gt;Lorem&lt;/div&gt;</pre>
    </div>
    {{EmbedLiveSample("sampleWinBorderlessGlass",100,50,"","", "nobutton")}}</td>
   <td>Firefox</td>
   <td>Firefox 64 で削除。このスタイルは要素に Aero Glass 効果を適用しますが、境界がありません。</td>
  </tr>
  <tr>
   <td><code>-moz-win-browsertabbar-toolbox</code> {{Non-standard_Inline}}</td>
   <td>
    <div class="hidden" id="sampleWinBrowsertabbarToolbox">
    <pre class="brush: css">
div { color: black;
-moz-appearance: -moz-win-browsertabbar-toolbox; }</pre>

    <pre class="brush: html">
&lt;div&gt;Lorem&lt;/div&gt;</pre>
    </div>
    {{EmbedLiveSample("sampleWinBrowsertabbarToolbox",100,50,"","", "nobutton")}}</td>
   <td>Firefox</td>
   <td>Firefox 64 で削除。このツールボックススタイルは、ブラウザーのタブバーに使用されることを想定しています。</td>
  </tr>
  <tr>
   <td><code>-moz-win-communicationstext</code> {{Non-standard_Inline}}</td>
   <td>
    <div class="hidden" id="sampleWinCommunicationstext">
    <pre class="brush: css">
div { color: black;
-moz-appearance: -moz-win-communicationstext; }</pre>

    <pre class="brush: html">
&lt;div&gt;Lorem&lt;/div&gt;</pre>
    </div>
    {{EmbedLiveSample("sampleWinCommunicationstext",100,50,"","", "nobutton")}}</td>
   <td>Firefox</td>
   <td>Firefox 64 で削除</td>
  </tr>
  <tr>
   <td><code>-moz-win-communications-toolbox</code> {{Non-standard_Inline}}</td>
   <td>
    <div class="hidden" id="sampleWinCommunicationsToolbox">
    <pre class="brush: css">
div { color: black;
-moz-appearance: -moz-win-communications-toolbox; }</pre>

    <pre class="brush: html">
&lt;div&gt;Lorem&lt;/div&gt;</pre>
    </div>
    {{EmbedLiveSample("sampleWinCommunicationsToolbox",100,50,"","", "nobutton")}}</td>
   <td>Firefox</td>
   <td>Firefox 64 で削除。このツールボックススタイルは、コミュニケーションと生産性アプリケーションに使用されることを想定しています。対応する前面色は <code>-moz-win-communicationstext</code> です。</td>
  </tr>
  <tr>
   <td><code>-moz-win-exclude-glass</code> {{Non-standard_Inline}}{{Gecko_MinVersion_Inline("6.0")}}</td>
   <td>
    <div class="hidden" id="sampleWinExcludeGlass">
    <pre class="brush: css">
div { color: black;
-moz-appearance: -moz-win-exclude-glass; }</pre>

    <pre class="brush: html">
&lt;div&gt;Lorem&lt;/div&gt;</pre>
    </div>
    {{EmbedLiveSample("sampleWinExcludeGlass",100,50,"","", "nobutton")}}</td>
   <td>Firefox</td>
   <td>Firefox 64 で削除。このスタイルは、要素に Aero Glass 効果を適用させないために使用します。</td>
  </tr>
  <tr>
   <td><code>-moz-win-glass</code> {{Non-standard_Inline}}</td>
   <td>
    <div class="hidden" id="sampleWinGlass">
    <pre class="brush: css">
div { color: black;
-moz-appearance: -moz-win-glass; }</pre>

    <pre class="brush: html">
&lt;div&gt;Lorem&lt;/div&gt;</pre>
    </div>
    {{EmbedLiveSample("sampleWinGlass",100,50,"","", "nobutton")}}</td>
   <td>Firefox</td>
   <td>Firefox 64 で削除。このスタイルは要素に Aero Glass 効果を適用します。</td>
  </tr>
  <tr>
   <td><code>-moz-win-media-toolbox</code> {{Non-standard_Inline}}</td>
   <td>
    <div class="hidden" id="sampleWinMediaToolbox">
    <pre class="brush: css">
div { color: black;
-moz-appearance: -moz-win-media-toolbox; }</pre>

    <pre class="brush: html">
&lt;div&gt;Lorem&lt;/div&gt;</pre>
    </div>
    {{EmbedLiveSample("sampleWinMediaToolbox",100,50,"","", "nobutton")}}</td>
   <td>Firefox</td>
   <td>Firefox 64 で削除。このツールボックススタイルは、メディアオブジェクトを管理するアプリケーションに使用されることを想定しています。対応する前面色は <code>-moz-win-mediatext</code> です。</td>
  </tr>
  <tr>
   <td><code>-moz-window-button-box</code> {{Non-standard_Inline}}</td>
   <td>
    <div class="hidden" id="sampleWindowButtonBox">
    <pre class="brush: css">
div { color: black;
-moz-appearance: -moz-window-button-box; }</pre>

    <pre class="brush: html">
&lt;div&gt;Lorem&lt;/div&gt;</pre>
    </div>
    {{EmbedLiveSample("sampleWindowButtonBox",100,50,"","", "nobutton")}}</td>
   <td>Firefox</td>
   <td>Firefox 64 で削除</td>
  </tr>
  <tr>
   <td><code>-moz-window-button-box-maximized</code> {{Non-standard_Inline}}</td>
   <td>
    <div class="hidden" id="sampleWindowButtonBoxMaximized">
    <pre class="brush: css">
div { color: black;
-moz-appearance: -moz-window-button-box-maximized; }</pre>

    <pre class="brush: html">
&lt;div&gt;Lorem&lt;/div&gt;</pre>
    </div>
    {{EmbedLiveSample("sampleWindowButtonBoxMaximized",100,50,"","", "nobutton")}}</td>
   <td>Firefox</td>
   <td>Firefox 64 で削除</td>
  </tr>
  <tr>
   <td><code>-moz-window-button-close</code> {{Non-standard_Inline}}</td>
   <td>
    <div class="hidden" id="sampleWindowButtonClose">
    <pre class="brush: css">
div { color: black;
-moz-appearance: -moz-window-button-close; }</pre>

    <pre class="brush: html">
&lt;div&gt;Lorem&lt;/div&gt;</pre>
    </div>
    {{EmbedLiveSample("sampleWindowButtonClose",100,50,"","", "nobutton")}}</td>
   <td>Firefox</td>
   <td>Firefox 64 で削除</td>
  </tr>
  <tr>
   <td><code>-moz-window-button-maximize</code> {{Non-standard_Inline}}</td>
   <td>
    <div class="hidden" id="sampleWindowButtonMaximize">
    <pre class="brush: css">
div { color: black;
-moz-appearance: -moz-window-button-maximize; }</pre>

    <pre class="brush: html">
&lt;div&gt;Lorem&lt;/div&gt;</pre>
    </div>
    {{EmbedLiveSample("sampleWindowButtonMaximize",100,50,"","", "nobutton")}}</td>
   <td>Firefox</td>
   <td>Firefox 64 で削除</td>
  </tr>
  <tr>
   <td><code>-moz-window-button-minimize</code> {{Non-standard_Inline}}</td>
   <td>
    <div class="hidden" id="sampleWindowButtonMinimize">
    <pre class="brush: css">
div { color: black;
-moz-appearance: -moz-window-button-minimize; }</pre>

    <pre class="brush: html">
&lt;div&gt;Lorem&lt;/div&gt;</pre>
    </div>
    {{EmbedLiveSample("sampleWindowButtonMinimize",100,50,"","", "nobutton")}}</td>
   <td>Firefox</td>
   <td>Firefox 64 で削除</td>
  </tr>
  <tr>
   <td><code>-moz-window-button-restore</code> {{Non-standard_Inline}}</td>
   <td>
    <div class="hidden" id="sampleWindowButtonRestore">
    <pre class="brush: css">
div { color: black;
-moz-appearance: -moz-window-button-restore; }</pre>

    <pre class="brush: html">
&lt;div&gt;Lorem&lt;/div&gt;</pre>
    </div>
    {{EmbedLiveSample("sampleWindowButtonRestore",100,50,"","", "nobutton")}}</td>
   <td>Firefox</td>
   <td>Firefox 64 で削除</td>
  </tr>
  <tr>
   <td><code>-moz-window-frame-bottom</code> {{Non-standard_Inline}}</td>
   <td>
    <div class="hidden" id="sampleWindowFrameBottom">
    <pre class="brush: css">
div { color: black;
-moz-appearance: -moz-window-frame-bottom; }</pre>

    <pre class="brush: html">
&lt;div&gt;Lorem&lt;/div&gt;</pre>
    </div>
    {{EmbedLiveSample("sampleWindowFrameBottom",100,50,"","", "nobutton")}}</td>
   <td>Firefox</td>
   <td>Firefox 64 で削除</td>
  </tr>
  <tr>
   <td><code>-moz-window-frame-left</code> {{Non-standard_Inline}}</td>
   <td>
    <div class="hidden" id="sampleWindowFrameLeft">
    <pre class="brush: css">
div { color: black;
-moz-appearance: -moz-window-frame-left; }</pre>

    <pre class="brush: html">
&lt;div&gt;Lorem&lt;/div&gt;</pre>
    </div>
    {{EmbedLiveSample("sampleWindowFrameLeft",100,50,"","", "nobutton")}}</td>
   <td>Firefox</td>
   <td>Firefox 64 で削除</td>
  </tr>
  <tr>
   <td><code>-moz-window-frame-right</code> {{Non-standard_Inline}}</td>
   <td>
    <div class="hidden" id="sampleWindowFrameRight">
    <pre class="brush: css">
div { color: black;
-moz-appearance: -moz-window-frame-right; }</pre>

    <pre class="brush: html">
&lt;div&gt;Lorem&lt;/div&gt;</pre>
    </div>
    {{EmbedLiveSample("sampleWindowFrameRight",100,50,"","", "nobutton")}}</td>
   <td>Firefox</td>
   <td>Firefox 64 で削除</td>
  </tr>
  <tr>
   <td><code>-moz-window-titlebar</code> {{Non-standard_Inline}}</td>
   <td>
    <div class="hidden" id="sampleWindowTitlebar">
    <pre class="brush: css">
div { color: black;
-moz-appearance: -moz-window-titlebar; }</pre>

    <pre class="brush: html">
&lt;div&gt;Lorem&lt;/div&gt;</pre>
    </div>
    {{EmbedLiveSample("sampleWindowTitlebar",100,50,"","", "nobutton")}}</td>
   <td>Firefox</td>
   <td>Firefox 64 で削除</td>
  </tr>
  <tr>
   <td><code>-moz-window-titlebar-maximized</code> {{Non-standard_Inline}}</td>
   <td>
    <div class="hidden" id="sampleWindowTitlebarMaximized">
    <pre class="brush: css">
div { color: black;
-moz-appearance: -moz-window-titlebar-maximized; }</pre>

    <pre class="brush: html">
&lt;div&gt;Lorem&lt;/div&gt;</pre>
    </div>
    {{EmbedLiveSample("sampleWindowTitlebarMaximized",100,50,"","", "nobutton")}}</td>
   <td>Firefox</td>
   <td>Firefox 64 で削除</td>
  </tr>
  <tr>
   <td><code>-apple-pay-button</code> {{Non-standard_Inline}}</td>
   <td>
    <div class="hidden" id="sampleApplePayButton">
    <pre class="brush: css">
div{ color: black;
-webkit-appearance: -apple-pay-button; }</pre>

    <pre class="brush: html">
&lt;div&gt;Lorem&lt;/div&gt;</pre>
    </div>
    {{EmbedLiveSample("sampleApplePayButton",100,50,"","", "nobutton")}}</td>
   <td>Safari</td>
   <td><strong>iOS and macOS only</strong>. Available on the web starting in iOS 10.1 and macOS 10.12.1</td>
  </tr>
 </tbody>
</table>

<h3 id="Formal_syntax" name="Formal_syntax">形式文法</h3>

{{CSSSyntax}}

<h2 id="Examples" name="Examples">例</h2>

<p>次のようにすると、要素を Firefox のツールバーボタンのように見せます。</p>

<pre class="brush: css">.exampleone {
  -moz-appearance: toolbarbutton;
}
</pre>

<p>カスタムスタイリングをラジオボタンとチェックボックス適用するための <code>appearance:none</code> の使用例を示す例は、<a href="http://jsfiddle.net/go392m5s/">このJSFiddle</a>も参照してください。</p>

<h2 id="Specifications" name="Specifications">仕様書</h2>

<table class="standard-table">
 <thead>
  <tr>
   <th scope="col">仕様書</th>
   <th scope="col">状態</th>
   <th scope="col">備考</th>
  </tr>
 </thead>
 <tbody>
  <tr>
   <td>{{SpecName("CSS4 Basic UI", "#appearance-switching", "appearance")}}</td>
   <td>{{Spec2("CSS4 Basic UI")}}</td>
   <td>初回定義</td>
  </tr>
 </tbody>
</table>

<p>{{CSSInfo}}</p>

<h2 id="Browser_compatibility" name="Browser_compatibility">ブラウザーの互換性</h2>

<p>{{Compat("css.properties.appearance")}}</p>

<h2 id="See_also" name="See_also">関連情報</h2>

<ul>
 <li><a class="external" href="http://www.w3.org/TR/2004/CR-css3-ui-20040511/#appearance">CSS 3 Basic User Interface での <code>appearance</code> の定義</a> (2004-05-11より Candidate Recommendation)。</li>
 <li><a class="external" href="http://wiki.csswg.org/spec/css4-ui#dropped-css3-features">UI 仕様 4 から削除された CSS3 機能</a></li>
</ul>