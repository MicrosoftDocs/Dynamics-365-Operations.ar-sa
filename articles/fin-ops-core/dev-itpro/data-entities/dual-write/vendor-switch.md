---
title: التبديل بين تصميمات المورّدين
description: توضح هذه المقالة كيفية التبديل بين تكامل بيانات المورد وبين تطبيقات التمويل والعمليات و Dataverse.
author: RamaKrishnamoorthy
ms.date: 09/20/2019
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: tfehr
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2020-01-06
ms.openlocfilehash: 5a1b3a6049e7e31e7e5bdcf690a766ecea8dc4b1
ms.sourcegitcommit: 6781fc47606b266873385b901c302819ab211b82
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 07/02/2022
ms.locfileid: "9112323"
---
# <a name="switch-between-vendor-designs"></a>التبديل بين تصميمات المورّدين

[!include [banner](../../includes/banner.md)]





## <a name="vendor-data-flow"></a>تدفق بيانات المورّد 

إذا اخترت استخدام جدول **الحساب** لتخزين الموردين من نوع **المؤسسة** وجدول **جهة الاتصال** لتخزين الموردين من نوع **الشخص** ، فقم بتكوين مهام سير العمل التالية. وإلا، فلن يكون هذا التكوين مطلوبًا.

## <a name="use-the-extended-vendor-design-for-vendors-of-the-organization-type"></a>استخدام تصميم المورد الموسع للموردين من نوع المؤسسة

تحتوي حزمة حل **Dynamics365FinanceExtended** على قوالب عملية سير العمل التالية. ستقوم بإنشاء سير عمل لكل قالب.

+ إنشاء الموردين في جدول الحسابات
+ إنشاء الموردين في جدول الموردين
+ تحديث الموردين في جدول الحسابات
+ تحديث الموردين في جدول الموردين

لإنشاء عمليات سير عمل جديدة باستخدام قوالب عملية سير العمل، اتبع الخطوات التالية.

1. أنشئ عملية سير عمل لجدول **المورد**، ثم حدد قالب عمل سير العمل **إنشاء الموردين في جدول الحسابات**. ثم حدد **موافق**. يعالج سير العمل هذا سيناريو إنشاء المورد لجدول **الحساب**.

    ![إنشاء الموردين في عملية سير عمل جدول الحسابات.](media/create_process.png)

2. أنشئ عملية سير عمل لجدول **المورد**، ثم حدد قالب عمل سير العمل **تحديث الموردين في جدول الحسابات**. ثم حدد **موافق**. يعالج سير العمل هذا سيناريو تحديث المورد لجدول **الحساب**.
3. أنشئ عملية سير عمل لجدول **الحساب**، ثم حدد قالب عمل سير العمل **إنشاء الموردين في جدول الموردين**.
4. أنشئ عملية سير عمل لجدول **الحساب**، ثم حدد قالب عمل سير العمل **تحديث الموردين في جدول الموردين**.
5. يمكنك تكوين مهام سير العمل بمثابه عمليات سير عمل في الوقت الحقيقي أو مهام سير العمل الخلفية وفقًا لمتطلباتك. لتكوين سير عمل كسير عمل خلفية، حدد **التحويل إلى سير عمل خلفية**.

    ![التحويل إلى زر سير عمل في الخلفية.](media/background_workflow.png)

6. قم بتنشيط مهام سير العمل التي قمت بإنشائها في جدولي **الحساب** و **المورد** لبدء استخدام الجدول **الحساب** لتخزين المعلومات للموردين من نوع **المؤسسة**.

## <a name="use-the-extended-vendor-design-for-vendors-of-the-person-type"></a>استخدام تصميم المورد الموسع للموردين من نوع الشخص

تحتوي حزمة حل **Dynamics365FinanceExtended** على قوالب عملية سير العمل التالية. ستقوم بإنشاء سير عمل لكل قالب.

+ إنشاء الموردين من نوع الشخص في جدول الموردين
+ إنشاء الموردين من نوع الشخص في جدول جهات الاتصال
+ تحديث الموردين من نوع الشخص في جدول جهات الاتصال
+ تحديث الموردين من نوع الشخص في جدول الموردين

لإنشاء عمليات سير عمل جديدة باستخدام قوالب عملية سير العمل، اتبع الخطوات التالية.

1. أنشئ عملية سير عمل لجدول **المورد**، ثم حدد قالب عمل سير العمل **إنشاء الموردين من نوع الشخص في جدول جهات الاتصال**. ثم حدد **موافق**. يعالج سير العمل هذا سيناريو إنشاء المورد لجدول **جهة الاتصال**.
2. أنشئ عملية سير عمل لجدول **المورد**، ثم حدد قالب عمل سير العمل **تحديث الموردين من نوع الشخص في جدول جهات الاتصال**. ثم حدد **موافق**. يعالج سير العمل هذا سيناريو تحديث المورد لجدول **جهة الاتصال**.
3. أنشئ عملية سير عمل لجدول **جهة الاتصال**، ثم حدد قالب **إنشاء الموردين من نوع الشخص في جدول الموردين**.
4. أنشئ عملية سير عمل لجدول **جهة الاتصال**، ثم حدد قالب **تحديث الموردين من نوع الشخص في جدول الموردين**.
5. يمكنك تكوين مهام سير العمل بمثابه عمليات سير عمل في الوقت الحقيقي أو مهام سير العمل الخلفية وفقًا لمتطلباتك. لتكوين سير عمل كسير عمل خلفية، حدد **التحويل إلى سير عمل خلفية**.
6. قم بتنشيط مهام سير العمل التي قمت بإنشائها في جدولي **جهة الاتصال** و **المورد** لبدء استخدام جدول **جهة الاتصال** لتخزين المعلومات للموردين من نوع **الشخص**.


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
