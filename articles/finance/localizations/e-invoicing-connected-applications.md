---
title: التطبيقات المتصلة
description: توضح هذه المقالة كيفية إعداد التطبيقات المتصلة في الفوترة الإلكترونية.
author: gionoder
ms.date: 02/07/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: gionoder
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.custom: ''
ms.assetid: ''
ms.search.form: ''
ms.openlocfilehash: f908caa902e4747d324480e3a5108b443d385ea7
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 08/12/2022
ms.locfileid: "9277320"
---
# <a name="connected-applications"></a>التطبيقات المتصلة

[!include [banner](../includes/banner.md)]

التطبيقات المتصلة هي مثيلات Microsoft Dynamics 365‎ Finance‏ و Dynamics 365 Supply Chain Management التي قد ترغب في الوصول إليها من خلال Regulatory Configuration Service‏ (‎RCS). من خلال التطبيقات المتصلة، يمكنك تكوين جزء من ميزة العولمة الخاصة بك في Finance أو Supply Chain Management لجعل سيناريو الفوترة الإلكترونية يعمل.

عند نشر ميزة العولمة الخاصة بك، يمكن نشر معلومات الإعداد التي تنطبق على تطبيق Finance أو Supply Chain Management مباشرةً من RCS إلى التطبيق المتصل المناسب.

يعد توفر معلمات Finance أو Supply Chain Management في RCS أمرًا مفيدًا عندما يكون لديك العديد من بيئات التطبيقات، مثل اختبار قبول المستخدم (UAT) وبيئات الإنتاج، وتريد الحفاظ على اتساق الإعداد من خلال نشر نفس المعلمات في بيئات مختلفة.

## <a name="create-a-connected-application"></a>إنشاء تطبيق متصل

1. سجل دخولك إلى حساب RCS.
2. في مساحة عمل **ميزات العولمة**، في قسم **البيئة**، حدد الإطار المتجانب **الفوترة الإلكترونية**.
3. في صفحة **إعداد البيئة**، في جزء الإجراء، حدد **التطبيقات المتصلة**.
4. حدد **جديد** لإنشاء تطبيق متصل.
5. في حقل **الاسم**، أدخل اسم التطبيق المراد الاتصال به.
6. في حقل **النوع** ، حدد **Dynamics 365 Finance**.
7. في حقل **التطبيق**، أدخل عنوان URL للبيئة المراد الاتصال بها.
8. في حقل **المستأجر**، حدد مستأجر البيئة.
9. حدد **حفظ**.
10. في جزء الإجراء ، حدد **فحص اتصال** لاختبار الاتصال مع البيئة. ثم أغلق الصفحة.

## <a name="link-connected-applications-to-environments"></a>ربط التطبيقات المتصلة بالبيئات

1. في صفحة **إعداد البيئة**، حدد **جديد** لتعيين تطبيق متصل لإحدى البيئات.
2. في حقل **التطبيق المتصل**، حدد أحد التطبيقات المتصلة.
3. في حقل **بيئة الخدمة**، حدد بيئة الخدمة.
4. حدد **حفظ** ثم قم بإغلاق الصفحة.
