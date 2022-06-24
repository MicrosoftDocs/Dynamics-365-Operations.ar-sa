---
title: قم بإعداد استيراد التسوية البنكية المتقدمة باستخدام التقارير الإلكترونية
description: توضح هذه المقالة كيفية استخدام التقارير الإلكترونية لإعداد عملية استيراد التسوية البنكية المتقدمة.
author: panolte
ms.date: 03/30/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BankStatementFormat
audience: Application User
ms.reviewer: twheeloc
ms.custom: 88433
ms.assetid: 73f3dcf6-040a-44ad-9512-7b3e0d17a571
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 10.0.25
ms.openlocfilehash: 2ac8811a5c10490d90f782472d3c198474c7edc0
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 06/03/2022
ms.locfileid: "8889109"
---
# <a name="set-up-advanced-bank-reconciliation-import-by-using-electronic-reporting"></a>قم بإعداد استيراد التسوية البنكية المتقدمة باستخدام التقارير الإلكترونية

[!include [banner](../includes/banner.md)]

تتيح لك ميزة التسوية المصرفية المتقدمة استيراد كشوف الحسابات البنكية الإلكترونية وتسويتها تلقائيًا مع المعاملات المصرفية في Microsoft Dynamics 365 Finance. توضح هذه المقالة كيفية إعداد وظيفة الاستيراد لكشوفات حساباتك البنكية. يختلف إعداد استيراد كشف الحساب البنكي، استنادًا إلى تنسيق كشف حسابك البنكي الإلكتروني. يدعم Microsoft Dynamics 365 Finance ثلاثة تنسيقات جاهزة لكشوف الحسابات: ISO20022 وMT940 وBAI2. 

## <a name="set-up-the-electronic-reporting-configuration"></a>إعداد تكوين التقارير الإلكترونية

1. انتقل إلى **مساحات العمل \> إعداد التقارير الإلكترونية**.
2. على الإطار المتجانب لموفر تكوين **Microsoft**، حدد **المستودعات**.
3. حدد **العمومي**، ثم حدد **فتح**.
4. إذا كان يجب إنشاء اتصال بالمستودع، فحدد الارتباط الأزرق في مربع الحوار.
5. في قائمة التكوين، ابحث عن **نموذج كشف حساب بنكي \> نموذج كشف حساب بنكي من BAI2**.
6. حدد تنسيق **BAI2**.
7. في علامة التبويب السريعة **إصدارات**، حدد أحدث إصدار، ثم حدد **استيراد**.

## <a name="set-up-the-bank-statement-format"></a>إعداد تنسيق كشف الحساب البنكي

1. انتقل إلى **إدارة النقد والبنوك \> إعداد \> إعداد التسوية البنكية المتقدمة‬ \> تنسيق كشف الحساب البنكي**.
2. حدد **جديد**.
3. قم بتعيين حقلي **تنسيق كشف الحساب** و **الاسم**.
4. حدد خانة الاختيار **تنسيق الاستيراد الإلكتروني العام**.
5. قم بتعيين حقل **استيراد تكوين التنسيق** إلى تنسيق **BAI2**.

## <a name="set-up-the-bank-account"></a>إعداد الحساب البنكي

1. انتقل إلى **إدارة النقد والبنوك \> الحسابات البنكية \> الحسابات البنكية**.
2. افتح الحساب البنكي.
3. في علامة التبويب السريعة **التسوية‬**، عيّن الخيار **تسوية بنكية متقدمة** إلى **نعم**.
4. عيّن الحقل **تنسيق كشف الحساب** إلى تنسيق **BAI2** الذي أنشأته سابقًا.

## <a name="import-the-bank-statement"></a>استيراد كشف الحساب البنكي

1. انتقل إلى **إدارة النقد والبنوك \> تسوية كشف الحساب البنكي \> كشوف الحسابات البنكية**.
2. في الجزء العلوي من صفحة **كشوف الحسابات البنكية**، حدد **استيراد كشف الحساب**.
3. عيّن حقل **الحساب البنكي** إلى الحساب البنكي في كشف الحساب.
4. عيّن الحقل **تنسيق كشف الحساب** إلى تنسيق **BAI2** الذي أنشأته سابقًا.
5. حدد **استعراض**، وحدد ملف **BAI**.
6. ثم حدد **تحميل**.
7. حدد **موافق** لاستيراد الملف المحدد.


## <a name="examples-of-bank-statement-formats-and-technical-layouts"></a>أمثلة عن تنسيقات كشوف الحسابات البنكية والتخطيطات التقنية
تجد أدناه أمثلة عن تعريفات التخطيط التقني لملفات استيراد التسوية البنكية المتقدمة وثلاثة ملفات أمثلة عن كشوفات الحسابات البنكية ذات الصلة: [أمثلة ملفات الاستيراد](//download.microsoft.com/download/8/e/c/8ec8d2d0-eb8c-41fb-ad8c-f01a4d670a44/Dynamics365FinanceAdvancedBankStatementLayouts.xlsx)  

| تعريف التخطيط التقني                             | ملف مثال عن كشف الحساب البنكي          |
|---------------------------------------------------------|--------------------------------------|
| DynamicsAXMT940Layout | [MT940StatementExample](//download.microsoft.com/download/2/d/c/2dcc4e55-ddc8-4a74-b79c-250fae201c3c/mt940StatementExample.txt)     |
| DynamicsAXISO20022Layout | [ISO20022StatementExample](https://nam06.safelinks.protection.outlook.com/?url=https%3A%2F%2Fdownload.microsoft.com%2Fdownload%2F1%2F5%2F5%2F155d84ed-c250-48f3-b0b1-c5a431e7855b%2FISO20022-MultipleStatements.xml&data=04%7C01%7CRobert.Schlomann%40microsoft.com%7C30d0c233cb6546547d0a08d8f4965edc%7C72f988bf86f141af91ab2d7cd011db47%7C1%7C0%7C637528273956712775%7CUnknown%7CTWFpbGZsb3d8eyJWIjoiMC4wLjAwMDAiLCJQIjoiV2luMzIiLCJBTiI6Ik1haWwiLCJXVCI6Mn0%3D%7C1000&sdata=3VzvLZK%2BO8PjuI7XVdC6rD2j3nUJfteo7zFp%2B1s9BwM%3D&reserved=0)             |
| DynamicsAXBAI2Layout    | [BAI2StatementExample](//download.microsoft.com/download/1/1/6/11693f57-bfc1-4993-a274-5fb978be70fa/BAI2StatementExample.txt)     |

