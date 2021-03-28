#### Document Control
| Date | Description | Author(s) |
| ---- | ----------- | --------- |
|      | 初譯        | 何宣慶    |
|      | 覆譯及審閱  | 柯智仁    |
|      | 發布        |           |



IPT:整合出版工具包

IPT: The Integrated Publishing Toolkit

*這是一個透過**GBIF**網路發表與分享生物多樣性資料集的免費公開下載軟體工具*

*A free open source software tool used to publish and share biodiversity datasets through the GBIF network.*

 

 

有關IPT

這個整合出版工具包(Integrated Publishing Toolkit)是一個用Java所寫的免費公開軟體工具，可以透過GBIF的網路發布或分享生物多樣性資料集。

如果想要知道IPT如何操作，可以試著看看這個簡短的25秒實際操作，告訴大家如何將資料集妥善地透過GBIF.org發表及登記。

[![img](file:////Users/cko/Library/Group%20Containers/UBF8T346G9.Office/TemporaryItems/msohtmlclip/clip_image002.png)](https://www.youtube.com/watch?v=eDH9IoTrMVE)

(如果無法點選Youtube頻道撥放，也可以[點此下載](https://videos.ctfassets.net/q553fnlofhvs/3iCjm4lxRSiCYE6Qq2A4GG/63b5690e48de42b0872ba4c25d629fe9/Introduction_to_publishing_using_the_GBIF_Integrated_Publishing_Toolkit__28IPT_29.mp4))

 

About the IPT

The Integrated Publishing Toolkit (IPT) is a free open source software tool written in Java that is used to publish and share biodiversity datasets through the GBIF network. The IPT can also be configured with either a DataCite or EZID account in order to assign DOIs to datasets transforming it into a data repository.

 

To understand how the IPT works, try watching this concise 25 minute live demo showing how a dataset gets properly published and registered through GBIF.org:

 

https://www.youtube.com/watch?v=eDH9IoTrMVE

 

(if you are unable to watch the video above, it can also be [downloaded directly](http://videos.contentful.com/q553fnlofhvs/3iCjm4lxRSiCYE6Qq2A4GG/63b5690e48de42b0872ba4c25d629fe9/Introduction_to_publishing_using_the_GBIF_Integrated_Publishing_Toolkit__28IPT_29.mp4))

 

**最新釋出版本****:2.3.6**

版本Version 2.3.6可以在這裡下載。

版本Version 2.3.6提升語言的覆蓋率，修正小錯誤以及更新版本的獨立性，藉以改善IPT的強度及安全性。

**Latest Release: 2.3.6**

Version 2.3.6 is available for download [here](http://repository.gbif.org/content/groups/gbif/org/gbif/ipt/2.3.6/ipt-2.3.6.war).

Version 2.3.6 improves coverage of translations, has [minor bug fixes](https://github.com/gbif/ipt/issues?q=is%3Aissue+milestone%3A2.3.6+is%3Aclosed) and updates dependency versions to improve the robustness and security of the IPT.

 

**版本****2.3.5****註釋**

版本2.3.5可以在這裡下載。

版本2.3.5修復了跨站字體漏洞，以及一個導致資料集清單的網路服務請求失敗問題。

**Notes from 2.3.5**

Version 2.3.5 is available for download [here](http://repository.gbif.org/content/groups/gbif/org/gbif/ipt/2.3.5/ipt-2.3.5.war).

Version 2.3.5 fixes cross site scripting vulnerabilities, and [an issue](https://github.com/gbif/ipt/issues/1344) that caused the dataset inventory web service request to fail.

 

**版本****2.3.4****註釋**

版本2.3.4包含一個IPT使用的Apache Struts web框架中發現的嚴重漏洞的安全更新。根據這篇文章，這是一個遠端控制碼執行漏洞，可能允許駭客在IPT伺服器上執行惡意命令。文章也提到駭客正積極地在使用這麼漏洞。因此我們建議所有使用者依照我們所發布的消息立刻更新版本。

您可以在這個部落格文章找到版本2.3.3更新的部分。

**Notes from 2.3.4**

Version 2.3.4 includes a security update that fixes a [critical vulnerability](https://struts.apache.org/docs/s2-045.html) that has been discovered in the Apache Struts web framework, which the IPT uses. According to [this article](http://thehackernews.com/2017/03/apache-struts-framework.html), this is a remote code execution vulnerability that could allow hackers to execute malicious commands on the IPT server. It also says that hackers are actively exploiting this vulnerability. **Therefore all users should plan to upgrade to this version immediately following the instructions in the** [**Release Notes**](https://github.com/gbif/ipt/wiki/IPTReleaseNotes233.wiki)**.**

You can find out what features were added in version 2.3.3 in [this blog post](http://gbif.blogspot.dk/2017/01/ipt-v233-your-repository-for.html).

 

**準備發表的版本****2.4**

目前並無版本2.4的發布期程。但您可以在此閱覽各種問題的進度。比較小的問題或安全性問題未來將會在後許發表的版本2.3.x中解決。

**Upcoming Release: 2.4**

No release date has been set yet for version 2.4, however, progress working on issues included in this release can be browsed [here](https://github.com/gbif/ipt/projects/2).

Minor issues and security issues will be addressed in patch releases for 2.3.x.

 

**致使用者**

  如果您只是對試用IPT感興趣，可以寄電子郵件到[helpdesk@gbif.org](mailto:helpdesk@gbif.org)取得測試版([Demo IPT](http://ipt.gbif.org/))的個人帳號。

  最簡單開始使用IPT的方法為在委託資料儲存中心([trusted data hosting centre](https://github.com/gbif/ipt/wiki/dataHostingCentres))請求一個帳號，可以讓您管理您的資料集以及透過GBIF.org發表，省去您用個人伺服器來設定以及管理的麻煩。當然，如果您要再點腦設定自己的IPT，可以到[Getting Started Guide](https://github.com/gbif/ipt/wiki/IPT2ManualNotes.wiki#getting-started-guide)依介紹開始使用。

*確認您有在*[IPT Mailing List](https://lists.gbif.org/mailman/listinfo/ipt/)*中註冊，該名單為支持**IPT**的使用者群組。**IPT**必須保持最新版本，且盡可能安全可靠。如您負責管理一個**IPT**，那麼您應該註冊以獲得新版本的通知，以便您可以立即更新。*

**@Users**

If you’re only interested in trying out the IPT please request an account on the [Demo IPT](http://ipt.gbif.org/) by sending an email to helpdesk@gbif.org.

The simplest way to begin using the IPT is to request a free account on a [trusted data hosting centre](https://github.com/gbif/ipt/wiki/dataHostingCentres) allowing you to manage your own datasets and publish them through GBIF.org without the hassle of setting up and maintaining the IPT on your own server.

Otherwise if want to setup your own instance of the IPT the [Getting Started Guide](https://github.com/gbif/ipt/wiki/IPT2ManualNotes.wiki#getting-started-guide) is your entry point.

*Be sure to sign up to the* [IPT Mailing List](https://lists.gbif.org/mailman/listinfo/ipt/)*, which serves as a support group for IPT users. It is essential that the IPT is kept up to date to be as secure and robust as possible, so if you are responsible for administering an IPT, then you should be signed up to be notified of new releases so that you can update immediately.*

 

**致翻譯人員**

  IPT的使用者介面及開放協同創作系統都需要國際化，然而這是一的公眾的努力，每一個人都歡迎加入。您可以在這裡針對翻譯人員完整的說明。

  感謝許多社群的努力以及透過[Crowdin](https://crowdin.com/project/gbif-ipt)本土化工具的強大功能，使用者介面現在已經被翻譯為七種不同語言，英文、法文、西班牙文、繁體中文、巴西文、葡萄牙文、日文及俄文。

**@Translators**

The IPT user interface and wiki both need internationalisation, but it’s a community effort and everyone is welcome to join. Full instructions aimed at translators can be found [here](https://github.com/gbif/ipt/wiki/HowToTranslate.wiki).

Thanks to an enormous community effort, and by leveraging the power of the [Crowdin](https://crowdin.com/project/gbif-ipt) localisation tool, the user interface has already been translated into seven different languages: English, French, Spanish, Traditional Chinese, Brazilian Portuguese, Japanese, and Russian.