# IPA登録サービスにおけるSASE・ZTNA・SWG対応状況（2026年11月15日時点）

## 結論

- **SASEに関連するIPA登録サービスを1件確認**：株式会社アクトの「Webセキュリティ Plus」（登録番号 **2025-201**、2類）。
- IPA登録情報の監視製品は **Check Point Harmony SASE-Internet Access**。Web通信保護、URLフィルタリング、マルウェア対策、EDR・SOC・保険を組み合わせる。
- この「Internet Access」はCheck Point公式資料により **SWG（Secure Web Gateway）機能**を持つと確認できる。
- **ZTNA（Private Access）機能を含む登録サービスであることは確認できていない**。Check PointのSASE製品群にZTNA機能があっても、この登録パッケージに含まれるとは限らない。
- **Cloudflare One / Cloudflare Zero Trust** が対象のIPA登録サービスに含まれることは、確認した公式一覧とサービス説明では裏付けられなかった。対象外と制度上確定したわけではない。

## 確認した登録サービス

| 項目 | 確認内容 |
| --- | --- |
| 登録サービス名 | Webセキュリティ Plus |
| 提供事業者 | 株式会社アクト（東京都） |
| IPA登録番号 | 2025-201 |
| 類型・監視 | 2類・端末監視 |
| 登録日 | 2025年10月1日 |
| 対象地域 | 全国 |
| 監視製品 | Check Point Harmony SASE-Internet Access |
| 構成 | SASEによるWeb通信保護、URLフィルタリング、マルウェア対策、EDR、SOC、サイバー保険 |
| 初期費用（税抜） | 60,000円 |
| 月額費用（税抜） | 1,580円（IPA掲載の1台当たり初年度試算：78,960円） |
| 最低契約期間 | 1年 |
| IT導入支援事業者登録 | 提供事業者の自社登録は「登録済み」とIPAに記載 |

**注意：** IPAへのサービス登録と、補助金事務局の「ITツール登録」は別の要件。実際の補助申請前に、対象のITツール登録番号・登録内容・最新の提供価格・ライセンス条件を提供事業者と補助金事務局のITツール検索で確認する必要がある。

### 機能別の判定

| 技術要素 | IPA登録サービスでの確認 | 根拠と留意点 |
| --- | --- | --- |
| SASE | **確認** | IPAが登録製品名に「Check Point Harmony SASE-Internet Access」と記載 |
| SWG | **確認** | Check Point公式管理ガイドがInternet Access内蔵SWGを記載 |
| ZTNA / Private Access | **未確認** | 登録サービスに明示された製品はInternet Access。Private Accessの提供範囲は要確認 |
| CASB / SaaS Security | **未確認** | Check Point製品群全体に機能があっても登録サービスに含まれるとは限らない |
| Cloudflare One / Zero Trust | **未確認** | IPA登録サービス比較表で明示的な記載を確認できなかった |

補足：別のIPA登録事業者（株式会社ウェバートン）の会社紹介には「SASE」への言及があるが、同社の登録サービス「Managed EDR-セキュアパックPL-EDR-U Ver1.1」の監視製品は「PIPELINE Managed EDR」。会社がSASEを扱っていることと、そのSASE商品がIPA登録済みであることは別である。

## 2類サービスとSASE

IPAは2024年3月に2類を創設した際、監視機能拡充の例として「クラウドサービスを対象とした異常監視（CASB、SASEなど）」を明示した。したがって**SASE技術を組み込むこと自体は制度の想定範囲内**。ただし、個別ベンダー製品・ライセンスが自動的に補助対象になるわけではない。

## デジタル化・AI導入補助金2026 セキュリティ対策推進枠

- **補助率**：中小企業 1/2以内、小規模事業者 2/3以内
- **補助額**：5万円～150万円
- **対象**：IPAのお助け隊サービスリスト掲載、かつ補助金事務局にITツール登録されたサービスの導入費用・サービス利用料（最大2年分）
- **第7次締切**：2026年12月1日（火）17:00（2026年11月15日時点の公式掲載）
- **留意点**：IPA登録があるだけでは申請できない。事務局のITツール登録・事業者要件・申請手続き・交付決定の確認が必要。交付決定前の契約・支払い等の可否も公募要領で確認する。

## Cloudflare Oneを補助金で導入したい場合の確認事項

1. 「Cloudflare One / Zero Trust」を含む登録済みお助け隊サービスが存在するかをIPA・販売事業者に確認する。
2. サービスがある場合、**IPA登録番号**と**2026年補助金事務局でのITツール登録状況**を確認する。
3. Cloudflare Oneのどの機能（Gateway/SWG、Access/ZTNA、CASB、DLPなど）と何ライセンス分が登録サービスの提供範囲に含まれるか確認する。
4. ライセンス単独調達ではなく、監視・相談・初動対応・保険等を含む登録パッケージとしての導入費用が補助対象か確かめる。
5. SASE全機能が必要なら、現在確認できている「Webセキュリティ Plus」は**Internet Access中心**なので、Private Access/ZTNA要件に足りるかを事前確認する。

## 一次資料（公式）

1. IPA：監視種別サービス一覧（更新日 2026-11-10）  
   https://www.ipa.go.jp/security/otasuketai-pr/hikaku/index.html
2. IPA：株式会社アクト・Webセキュリティ Plus（登録番号 2025-201）  
   https://www.ipa.go.jp/security/otasuketai-pr/hikaku/service/2022-020.html
3. IPA：2類の制度説明（CASB・SASEを監視拡充例に明示）  
   https://www.ipa.go.jp/archive/press/2023/press20240315.html
4. Check Point：Internet Access 管理ガイド（内蔵SWG）  
   https://sc1.checkpoint.com/documents/Infinity_Portal/WebAdminGuides/EN/SASE-Admin-Guide/SASE_Security/Topics/internet_access/internet_access_overview_and_swg_capabilities.html
5. IPA：ウェバートン登録サービス（会社説明と登録対象の区別）  
   https://www.ipa.go.jp/security/otasuketai-pr/hikaku/service/2024-007.html
6. デジタル化・AI導入補助金2026：セキュリティ対策推進枠  
   https://it-shien.smrj.go.jp/applicant/subsidy/security
7. デジタル化・AI導入補助金2026：ITツール登録要件  
   https://it-shien.smrj.go.jp/itvendor/procedure/ittool/

---
調査日：2026-11-15。これは公式資料を個別確認した現時点の調査メモであり、別途進行中のDeep Researchの完成レポートを転載したものではありません。
