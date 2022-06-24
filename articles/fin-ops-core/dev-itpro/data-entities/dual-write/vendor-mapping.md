---
title: أصل المورّد المتكامل
description: توفر هذه المقالة تكامل بيانات المورّد بين تطبيقات Finance and Operations و Dataverse.
author: RamaKrishnamoorthy
ms.date: 07/15/2019
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: tfehr
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2019-07-15
ms.openlocfilehash: 394bb19000076eace6377e07bb3a939c8345da8a
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 06/03/2022
ms.locfileid: "8905304"
---
# <a name="integrated-vendor-master"></a>أصل المورّد المتكامل

[!include [banner](../../includes/banner.md)]



يشير مصطلح *المورد* إلى مؤسسة مورد أو مالك وحيد يقدم بضائع أو خدمات لشركة. وعلى الرغم من أن *المورّد* عبارة عن مفهوم تم إنشاؤه في Microsoft Dynamics 365 Supply Chain Management، إلا أن مفهوم المورّد غير موجود في تطبيقات customer engagement. ومع ذلك، يمكنك زيادة تحميل جدول **الحساب/جهة الاتصال** لتخزين معلومات المورد. يقدم أصل المورد المتكامل مفهوم مورد صريحًا في تطبيقات customer engagement. يمكنك إما استخدام بيانات تصميم المورد الجديد أو مورد المتجر في جدول **الحساب/جهة الاتصال**. تدعم الكتابة الثنائية كلا الأسلوبين.

وفي كلتا الحالتين، يتم دمج بيانات المورد بين Dynamics 365 Supply Chain Management، وDynamics 365 Sales، وDynamics 365 Field Service، ومداخل Power Apps. في Supply Chain Management، تتوفر البيانات لمهام سير العمل مثل طلبات الشراء وأوامر الشراء.

## <a name="vendor-data-flow"></a>تدفق بيانات المورّد

إذا كنت ترغب في تخزين بيانات المورد في جدول **الحساب/جهة الاتصال** في Dataverse، يمكنك استخدام تصميم المورد الجديد.

![تدفق بيانات المورّد.](media/dual-write-vendor-data-flow.png)

إذا كنت ترغب في مواصلة تخزين بيانات المورد في جدول **الحساب/جهة الاتصال**، يمكنك استخدام تصميم المورد الموسع. لاستخدام تصميم المورد الموسع، يجب تكوين عمليات سير عمل المورد في حزمة حلول الكتابة الثنائية. لمزيد من المعلومات، راجع [التبديل بين تصميمات الموردين](vendor-switch.md).

![تدفق بيانات المورّد الموسّعة.](media/dual-write-vendor-detail.jpg)

> [!TIP]
> إذا كنت تستخدم مداخل Power Apps لموردي الخدمة الذاتية، فيمكن لمعلومات المورد التدفق مباشرةً إلى تطبيقات التمويل والعمليات.

## <a name="templates"></a>القوالب

تتضمن بيانات المورّد كافة المعلومات المتعلقة بالمورّد، مثل مجموعة المورّدين والعناوين ومعلومات الاتصال وملف تعريف الدفع وملف تعريف الفاتورة. تعمل مجموعة من مخططات الجداول معًا أثناء تفاعل بيانات المورّد، كما هو موضح في الجدول التالي.

تطبيقات Finance and Operations | تطبيقات Customer Engagement     | الوصف
----------------------------|-----------------------------|------------
[جهات اتصال CDS V2](mapping-reference.md#115) | جهات الاتصال | يقوم هذا القالب بمزامنة كافة معلومات جهات الاتصال الاساسيه والثانوية والثلاثية لكل من العملاء والموردين.
[ملحقات الاسم](mapping-reference.md#155) | msdyn_nameaffixes | يقوم هذا القالب بمزامنة البيانات المرجعية لملصقات الأسماء، لكلٍّ من العملاء والموردين.
[بنود يوم الدفع CDS V2](mapping-reference.md#157) | msdyn_paymentdaylines | يقوم هذا القالب بمزامنة البيانات المرجعية لأسطر أيام الدفع لكلٍّ من العملاء والموردين.
[أيام الدفع CDS](mapping-reference.md#158) | msdyn_paymentdays | يقوم هذا القالب بمزامنة البيانات المرجعية لأيام الدفع لكلٍّ من العملاء والموردين.
[بنود جدول الدفع](mapping-reference.md#159) | msdyn_paymentschedulelines | مزامنة البيانات المرجعية لأسطر جداول الدفع لكلٍّ من العملاء والموردين.
[جدول الدفع](mapping-reference.md#160) | msdyn_paymentschedules | يقوم هذا القالب بمزامنة البيانات المرجعية لجدول الدفع لكلٍّ من العملاء والموردين.
[شروط الدفع](mapping-reference.md#161) | msdyn_paymentterms | يقوم هذا القالب بمزامنة البيانات المرجعية لمدد الدفع (مدد الدفع) لكلٍّ من العملاء والموردين.
[موردو V2](mapping-reference.md#202) | msdyn_vendors | بإمكان الشركات التي تستخدم حلاً مخصصًا للمورّدين الاستفادة من مفهوم المورّد المبتكر الذي تم تقديمه في Dataverse بسبب تكامل تطبيقات Finance and Operations.
[مجموعات الموردين](mapping-reference.md#200) | msdyn_vendorgroups | يقوم هذا القالب بمزامنة معلومات مجموعة الموردين.
[طريقة دفع المورّد](mapping-reference.md#201) | msdyn_vendorpaymentmethods | يقوم هذا القالب بمزامنة معلومات طرق دفع الموردين.

[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
