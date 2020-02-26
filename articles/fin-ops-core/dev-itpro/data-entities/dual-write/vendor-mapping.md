---
title: أصل المورّد المتكامل
description: يوضح هذا الموضوع تكامل بيانات المورد بين تطبيقات Finance and Operations وCommon Data Service.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 07/15/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2019-07-15
ms.openlocfilehash: 2442a6869daac22a435c1a7504b93ea4b5c14747
ms.sourcegitcommit: 54baab2a04e5c534fc2d1fd67b67e23a152d4e57
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 02/04/2020
ms.locfileid: "3019614"
---
# <a name="integrated-vendor-master"></a>أصل المورّد المتكامل

[!include [banner](../../includes/banner.md)]

[!include [preview-banner](../../includes/preview-banner.md)]

يشير المصطلح *المورّد* إلى مؤسسه مورّد أو مالك وحيد يعتبر جزءًا من عملية سلسلة التوريد ويوفر السلع للشركات. وعلى الرغم من أن *المورّد* عبارة عن مفهوم تم إنشاؤه في تطبيقات Finance and Operations، فإن مفهوم المورّد غير موجود في تطبيقات Dynamics 365 الأخرى. بدلا من ذلك، تقوم بعض الشركات بإجراء تحميل زائد على لكيان الحساب بتخزين معلومات العملاء ومعلومات المورّدين على حد سواء. وتستخدم شركات أخرى مفهومًا مخصصًا للمورّد. يدعم تكامل Common Data Service هذين التصميمين. وبالتالي، يمكنك تمكين أي واحد من التصميمين، بحسب سيناريو شركتك.

تتيح لك امكانيه تكامل بيانات المورّد بين تطبيقات Finance and Operations وتطبيقات Dynamics 365 الأخرى بإجراء إدارة متعددة للبيانات. بغض النظر عن مصدر بيانات المورّدين، فهي تتكامل في الخلفية عبر حدود التطبيق واختلافات البنية التحتية. 

### <a name="vendor-data-flow"></a>تدفق بيانات المورّد

إذا أردت استخدام تطبيقات Dynamics 365 الأخرى لإدارة المورّدين، وأردت عزل معلومات المورّد عن معلومات العميل، فيمكنك استخدام تصميم المورّد الجديد.

![تدفق بيانات المورّد](media/dual-write-vendor-data-flow.png)

إذا أردت استخدام تطبيقات Dynamics 365 الأخرى لإدارة المورّدين، وأردت متابعة استخدام كيان الحساب لتخزين معلومات المورّدين، فيمكنك استخدام تصميم المورّد الموسع الجديد. في هذا التصميم، يتم تخزين معلومات المورّد الموسعة، مثل مجموعة المورّد ومعلومات ملف تعريف ترحيل المورّد، في تفاصيل المورّد‬.

![تدفق بيانات المورّد الموسّعة](media/dual-write-vendor-detail.jpg)

تشبه معلومات اتصال المورّد معلومات اتصال العميل. في الخلفية، يتم تخزين معلومات جهة الاتصال واستردادها من الكيانات نفسها.

## <a name="templates"></a>القوالب

تتضمن بيانات المورّد كافة المعلومات المتعلقة بالمورّد، مثل مجموعة المورّدين والعناوين ومعلومات الاتصال وملف تعريف الدفع وملف تعريف الفاتورة. تعمل مجموعة من مخططات الكيانات معًا أثناء تفاعل بيانات المورّد، كما هو موضح في الجدول التالي.

تطبيقات Finance and Operations | تطبيقات Dynamics 365 الأخرى         | ‏‏الوصف
----------------------------|---------------------------------|------------
المورّد V2               | الحساب | بإمكان الشركات التي تستخدم كيان الحساب لتخزين معلومات المورّد متابعة استخدامها بالطريقة نفسها. ويمكنها أيضًا الاستفادة من وظيفة المورّد الصريحة التي تأتي بسبب تكامل تطبيقات Finance and Operations.
المورّد V2               | Msdyn\_vendors | بإمكان الشركات التي تستخدم حلاً مخصصًا للمورّدين الاستفادة من مفهوم المورّد المبتكر الذي تم تقديمه في Common Data Service بسبب تكامل تطبيقات Finance and Operations. 
مجموعات الموردين | msdyn_vendorgroups | يقوم هذا القالب بمزامنة معلومات مجموعة الموردين.
طريقة دفع المورّد | msdyn_vendorpaymentmethods | يقوم هذا القالب بمزامنة معلومات طرق دفع الموردين.
جهات اتصال CDS V2             | جهات الاتصال                        | يقوم قالب [جهات الاتصال](customer-mapping.md#cds-contacts-v2-to-contacts) بمزامنة كافة معلومات جهات الاتصال الاساسيه والثانوية والثلاثية لكل من العملاء والموردين.
بنود جدول الدفع      | msdyn_paymentschedulelines      | يقوم قالب [أسطر جدول الدفع](customer-mapping.md#payment-schedule-lines-to-msdyn_paymentschedulelines) بمزامنة البيانات المرجعية للعملاء والموردين.
جدول الدفع            | msdyn_paymentschedules          | يقوم قالب [جداول الدفع](customer-mapping.md#payment-schedule-to-msdyn_paymentschedules) بمزامنة البيانات المرجعية لجدول الدفع للعملاء والموردين.
بنود يوم الدفع CDS V2    | msdyn_paymentdaylines           | يقوم قالب [أسطر أيام الدفع](customer-mapping.md#payment-day-lines-cds-v2-to-msdyn_paymentdaylines) بمزامنة البيانات المرجعية لأسطر أيام الدفع للعملاء والموردين.
أيام الدفع CDS            | msdyn_paymentdays               | يقوم قالب [أيام الدفع](customer-mapping.md#payment-days-cds-to-msdyn_paymentdays) بمزامنة البيانات المرجعية لأيام الدفع، لكلٍّ من العملاء والموردين.
شروط الدفع            | msdyn_paymentterms              | يقوم قالب [مدد الدفع](customer-mapping.md#terms-of-payment-to-msdyn_paymentterms) بمزامنة البيانات المرجعية لمدد الدفع لكلٍّ من العملاء والموردين.
ملحقات الاسم                | msdyn_nameaffixes               | يقوم قالب [ملصقات الأسماء](customer-mapping.md#name-affixes-to-msdyn_nameaffixes) بمزامنة البيانات المرجعية لملصقات الأسماء، لكلٍّ من العملاء والموردين.

[!include [symbols](../../includes/dual-write-symbols.md)]

[!include [Vendors](includes/VendorsV2-msdyn-vendors.md)]

[!include [Vendor groups](includes/VendVendorGroup-msdyn-vendorgroups.md)]

[!include [Vendor payment methods](includes/VendorPaymentMethod-msdyn-vendorpaymentmethods.md)]
