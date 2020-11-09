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
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2019-07-15
ms.openlocfilehash: 5c4cc92fd7809f4016d8421c98f41a85fcfedc7b
ms.sourcegitcommit: 0a741b131ed71f6345d4219a47cf5f71fec6744b
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 10/13/2020
ms.locfileid: "3997632"
---
# <a name="integrated-vendor-master"></a>أصل المورّد المتكامل

[!include [banner](../../includes/banner.md)]



يشير مصطلح *المورد* إلى مؤسسة مورد أو مالك وحيد يقدم بضائع أو خدمات لشركة. وعلى الرغم من أن *المورّد* عبارة عن مفهوم تم إنشاؤه في Microsoft Dynamics 365 Supply Chain Management، إلا أن مفهوم المورّد غير موجود في التطبيقات المستندة إلى النماذج في Dynamics 365. ومع ذلك، يمكنك زيادة تحميل كيان **الحساب/جهة الاتصال** لتخزين معلومات المورد. يقدم أصل المورد المتكامل مفهوم مورد صريحًا في التطبيقات المستندة إلى النماذج في Dynamics 365. يمكنك إما استخدام بيانات تصميم المورد الجديد أو مورد المتجر في كيان **الحساب/جهة الاتصال**. تدعم الكتابة الثنائية كلا الأسلوبين.

وفي كلتا الحالتين، يتم دمج بيانات المورد بين Dynamics 365 Supply Chain Management، وDynamics 365 Sales، وDynamics 365 Field Service، ومداخل Power Apps. في Supply Chain Management، تتوفر البيانات لمهام سير العمل مثل طلبات الشراء وأوامر الشراء.

## <a name="vendor-data-flow"></a>تدفق بيانات المورّد

إذا كنت ترغب في تخزين بيانات المورد في كيان **الحساب/جهة الاتصال** في Common Data Service، يمكنك استخدام تصميم المورد الجديد.

![تدفق بيانات المورّد](media/dual-write-vendor-data-flow.png)

إذا كنت ترغب في مواصلة تخزين بيانات المورد في كيان **الحساب/جهة الاتصال** ، يمكنك استخدام تصميم المورد الموسع. لاستخدام تصميم المورد الموسع، يجب تكوين عمليات سير عمل المورد في حزمة حلول الكتابة الثنائية. لمزيد من المعلومات، راجع [التبديل بين تصميمات الموردين](vendor-switch.md).

![تدفق بيانات المورّد الموسّعة](media/dual-write-vendor-detail.jpg)

> [!TIP]
> إذا كنت تستخدم مداخل Power Apps لموردي الخدمة الذاتية، فيمكن لمعلومات المورد التدفق مباشرةً إلى تطبيقات Finance and Operations.

## <a name="templates"></a>القوالب

تتضمن بيانات المورّد كافة المعلومات المتعلقة بالمورّد، مثل مجموعة المورّدين والعناوين ومعلومات الاتصال وملف تعريف الدفع وملف تعريف الفاتورة. تعمل مجموعة من مخططات الكيانات معًا أثناء تفاعل بيانات المورّد، كما هو موضح في الجدول التالي.

تطبيقات Finance and Operations | تطبيقات Dynamics 365 الأخرى     | ‏‏الوصف
----------------------------|-----------------------------|------------
المورّد V2                   | الحساب                     | بإمكان الشركات التي تستخدم كيان الحساب لتخزين معلومات المورّد متابعة استخدامها بالطريقة نفسها. ويمكنها أيضًا الاستفادة من وظيفة المورّد الصريحة التي تأتي بسبب تكامل تطبيقات Finance and Operations.
المورّد V2                   | Msdyn\_vendors              | بإمكان الشركات التي تستخدم حلاً مخصصًا للمورّدين الاستفادة من مفهوم المورّد المبتكر الذي تم تقديمه في Common Data Service بسبب تكامل تطبيقات Finance and Operations. 
مجموعات الموردين               | msdyn\_vendorgroups         | يقوم هذا القالب بمزامنة معلومات مجموعة الموردين.
طريقة دفع المورّد       | msdyn\_vendorpaymentmethods | يقوم هذا القالب بمزامنة معلومات طرق دفع الموردين.
جهات اتصال CDS V2             | جهات الاتصال                    | يقوم قالب [جهات الاتصال](customer-mapping.md#cds-contacts-v2-to-contacts) بمزامنة كافة معلومات جهات الاتصال الاساسيه والثانوية والثلاثية لكل من العملاء والموردين.
بنود جدول الدفع      | msdyn\_paymentschedulelines | يقوم قالب [أسطر جدول الدفع](customer-mapping.md#payment-schedule-lines-to-msdyn_paymentschedulelines) بمزامنة البيانات المرجعية للعملاء والموردين.
جدول الدفع            | msdyn\_paymentschedules     | يقوم قالب [جداول الدفع](customer-mapping.md#payment-schedule-to-msdyn_paymentschedules) بمزامنة البيانات المرجعية لجدول الدفع للعملاء والموردين.
بنود يوم الدفع CDS V2    | msdyn\_paymentdaylines      | يقوم قالب [أسطر أيام الدفع](customer-mapping.md#payment-day-lines-cds-v2-to-msdyn_paymentdaylines) بمزامنة البيانات المرجعية لأسطر أيام الدفع للعملاء والموردين.
أيام الدفع CDS            | msdyn\_paymentdays          | يقوم قالب [أيام الدفع](customer-mapping.md#payment-days-cds-to-msdyn_paymentdays) بمزامنة البيانات المرجعية لأيام الدفع، لكلٍّ من العملاء والموردين.
شروط الدفع            | msdyn\_paymentterms         | يقوم قالب [مدد الدفع](customer-mapping.md#terms-of-payment-to-msdyn_paymentterms) بمزامنة البيانات المرجعية لمدد الدفع لكلٍّ من العملاء والموردين.
ملحقات الاسم                | msdyn\_nameaffixes          | يقوم قالب [ملصقات الأسماء](customer-mapping.md#name-affixes-to-msdyn_nameaffixes) بمزامنة البيانات المرجعية لملصقات الأسماء، لكلٍّ من العملاء والموردين.

[!include [symbols](../../includes/dual-write-symbols.md)]

[!include [Vendors](includes/VendorsV2-msdyn-vendors.md)]

[!include [Vendor groups](includes/VendVendorGroup-msdyn-vendorgroups.md)]

[!include [Vendor payment methods](includes/VendorPaymentMethod-msdyn-vendorpaymentmethods.md)]
