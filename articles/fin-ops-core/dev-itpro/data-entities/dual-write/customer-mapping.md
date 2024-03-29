---
title: أصل العميل المتكامل
description: توضح هذه المقالة تكامل بيانات العميل بين تطبيقات التمويل والعمليات وDataverse.
author: RamaKrishnamoorthy
ms.date: 07/15/2019
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2019-07-15
ms.openlocfilehash: ea142aff7c8f4b442d7224325e44359129efe8a8
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 08/12/2022
ms.locfileid: "9289669"
---
# <a name="integrated-customer-master"></a>أصل العميل المتكامل

[!include [banner](../../includes/banner.md)]



يمكن إدارة بيانات العملاء في أكثر من تطبيق Dynamics 365 واحد. علي سبيل المثال، يمكن أن ينشأ صف العميل إذا كان نشاط المبيعات في Dynamics 365 Sales (تطبيق customer engagement)، أو يمكن أن صف من خلال نشاط بيع بالتجزئة في Dynamics 365 Commerce (تطبيق finance and operations). بغض النظر عن مكان إنشاء بيانات العميل ، يتم دمجها خلف الكواليس. يوفر أصل العميل المتكامل المرونة لبيانات العميل الرئيسية في أي تطبيق Dynamics 365 ويوفر طريقة عرض شاملة للعميل عبر مجموعة تطبيقات Dynamics 365.

## <a name="customer-data-flow"></a>تدفق بيانات العميل

*العميل* هو مفهوم معرف بشكل دقيق في التطبيقات. ولذلك، فإن تكامل بيانات العميل ينطوي فقط على مواءمة مفهوم العميل بين التطبيقين. يبين الرسم التوضيحي التالي تدفق بيانات العميل.

![تدفق بيانات العميل.](media/dual-write-customer-data-flow.png)

يمكن تصنيف العملاء على نطاق واسع في نوعين: العملاء التجاريين/المؤسسيين والمستهلكين/المستخدمين النهائيين. يتم تخزين هذين النوعين من العملاء والتعامل معهم بطريقة مختلفة في تطبيقات التمويل والعمليات وDataverse.

في التمويل والعمليات، تتم إدارة العملاء التجاريين/المؤسسات والمستهلكين/المستخدمين النهائيين في جدول واحد يسمى **CustTable** (CustCustomerV3Entity)، ويتم تصنيفهم استنادًا إلى سمة **النوع**. (إذا تم تعيين **النوع** إلى **مؤسسة**، فسيكون العميل تجاريًا/مؤسسيًا، وإذا تم تعيين **النوع** إلى **شخص**، فسيكون العميل مستهلكًا/مستخدمًا نهائيًا.) يتم التعامل مع معلومات جهة الاتصال الرئيسية عبر الجدول SMMContactPersonEntity.

في Dataverse، تتم إدارة العملاء التجاريين/المؤسسيين في جدول الحساب، ويتم تعريفهم كعملاء عند تعيين سمة **RelationshipType** إلى **عميل**. يتم تمثيل المستهلكين/المستخدمين النهائيين وشخص جهة الاتصال بواسطة جدول جهة الاتصال. للفصل بشكل واضح بين المستهلك/المستخدم النهائي وشخص جهة الاتصال، يتضمن جدول **جهة الاتصال** علامة منطقية تسمى **قابل للبيع**. عندما تكون قيمة **قابل للبيع** **صواب**، تكون جهة الاتصال عبارة عن عميل مستهلك/مستخدم نهائي، ولا يمكن إنشاء الأوامر وعروض الأسعار لجهة الاتصال هذه. عندما تكون قيمة **قابل للبيع** **خطأ**، تكون جهة الاتصال مجرد جهة اتصال رئيسية للعميل.

عندما تشارك جهة اتصال غير قابلة للبيع في عملية عرض أسعار أو أمر، يتم تعيين قيمة **قابل للبيع** إلى **صواب** لوضع علامة على جهة الاتصال كجهة اتصال قابلة للبيع. جهة الاتصال التي أصبح جهة اتصال قابلة للبيع تبقى جهة اتصال قابلة للبيع.

## <a name="templates"></a>القوالب

تتضمن بيانات العميل كافة المعلومات المتعلقة بالعميل، مثل مجموعة العملاء والعناوين ومعلومات الاتصال وملف تعريف الدفع وملف تعريف الفاتورة وحالة الولاء. تعمل مجموعة من مخططات الجداول معًا أثناء تفاعل بيانات العميل، كما هو موضح في الجدول التالي.

تطبيقات Finance and Operations | تطبيقات Customer Engagement         | الوصف
----------------------------|---------------------------------|------------
[جهات اتصال CDS V2](mapping-reference.md#115) | جهات الاتصال | يقوم هذا القالب بمزامنة كافة معلومات جهات الاتصال الاساسيه والثانوية والثلاثية لكل من العملاء والموردين.
[مجموعات العملاء](mapping-reference.md#126) | msdyn_customergroups | يقوم هذا القالب بمزامنة معلومات مجموعة العملاء.
[طريقة دفع العميل](mapping-reference.md#127) | msdyn_customerpaymentmethods | يقوم هذا القالب بمزامنة معلومات طرق دفع العملاء.
[العملاء V3](mapping-reference.md#101) | الحسابات | يقوم هذا القالب بمزامنة المعلومات الرئيسية للعميل للعملاء التجاريين والمؤسسين.
[العملاء V3](mapping-reference.md#116) | جهات الاتصال | يقوم هذا القالب بمزامنة البيانات الرئيسية للعميل للعملاء والمستخدمين النهائيين.
[ملحقات الاسم](mapping-reference.md#155) | msdyn_nameaffixes | يقوم هذا القالب بمزامنة البيانات المرجعية لملصقات الأسماء، لكلٍّ من العملاء والموردين.
[بنود يوم الدفع CDS V2](mapping-reference.md#157) | msdyn_paymentdaylines | يقوم هذا القالب بمزامنة البيانات المرجعية لأسطر أيام الدفع لكلٍّ من العملاء والموردين.
[أيام الدفع CDS](mapping-reference.md#158) | msdyn_paymentdays | يقوم هذا القالب بمزامنة البيانات المرجعية لأيام الدفع لكلٍّ من العملاء والموردين.
[بنود جدول الدفع](mapping-reference.md#159) | msdyn_paymentschedulelines | مزامنة البيانات المرجعية لأسطر جداول الدفع لكلٍّ من العملاء والموردين.
[جدول الدفع](mapping-reference.md#160) | msdyn_paymentschedules | يقوم هذا القالب بمزامنة البيانات المرجعية لجدول الدفع لكلٍّ من العملاء والموردين.
[شروط الدفع](mapping-reference.md#161) | msdyn_paymentterms | يقوم هذا القالب بمزامنة البيانات المرجعية لمدد الدفع (مدد الدفع) لكلٍّ من العملاء والموردين.

[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]

