---
title: قائمه ميزات الضريبة الفارغة في معلمات حساب الضريبة
description: توضح هذه المقالة كيفية استكشاف مشكلة وجود قائمة ميزات الضريبة في صفحة معلمات حساب الضريبة الفارغة وإصلاحها.
author: wangchen
ms.date: 03/04/2022
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: TaxIntegrationTaxServiceParameters
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: wangchen
ms.search.validFrom: 2021-10-26
ms.dyn365.ops.version: Version 10.0.21
ms.openlocfilehash: 0d9286ec313a270da86181ff80ddfd690a757c9b
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 06/03/2022
ms.locfileid: "8869941"
---
# <a name="empty-tax-feature-list-in-tax-calculation-parameters"></a>قائمه ميزات الضريبة الفارغة في معلمات حساب الضريبة

[!include [banner](../includes/banner.md)]


## <a name="symptom"></a>العَرَضْ

لقد قمت بنشر ميزة في Regulatory Configuration Service (RCS)، بحيث يمكنك استخدامها في 365 Finance Microsoft Dynamics. ومع ذلك عند قيامك بفتح Finance، انتقل إلى **الضريبة** \> **الإعداد** \> **تكوين الضريبة** \> **معلمات حساب الضريبة**، وحاول تحديد قيمة في حقل **اسم إعداد الميزة**، تكون قائمة القيم فارغة.

## <a name="reason"></a>السبب

تحدث هذه المشكلة عادةً لأن بيئة التمويل وبيئة RCS ليست ضمن نفس المستأجر.

### <a name="rcs-tenant"></a>مستأجر RCS

اتبع هذه الخطوات للعثور على معرف مستأجر RCS الخاص بك.

1. انسخ عنوان URL لـ RCS الكامل. على سبيل المثال، قد يكون عنوان URL `https://rcs-rts-sf-ed22b5aeea8-int-westus2.configure.global.int.dynamics.com/namespaces/817ff7a0-0d77-4aba-9360-3c9749e2c5de/?cmp=dat&mi=RCSFeatureDomainsWorkspace`.
2. افتح نافذة مستعرض InPrivate، والصق عنوان URL لـ RCS في شريط العناوين، ثم حدد **Enter**. يتم توجيهك إلى صفحة تسجيل الدخول، حيث يمكنك العثور على معرف مستأجر RCS. على سبيل المثال، إذا كان عنوان URL لصفحة تسجيل الدخول هو `https://login.microsoftonline.com/d335a570-a05b-4bc5-8eb3-c42c65f9560d` فإن معرف المستأجر هو المعلومات التي تظهر بعد `https://login.microsoftonline.com/`، أو **d335a570-a05b-4bc5-8eb3-c42c65f9560d**.

### <a name="finance-environment-tenant-id"></a>معرف مستأجر بيئة Finance

للعثور على معرّف المستأجر لبيئة التمويل لديك، اتبع نفس الخطوات التي اتبعتها للعثور على مستأجر RCS. ومع ذلك، انسخ والصق عنوان URL الكامل لبيئة التمويل لديك بدلاً من عنوان URL الكامل لـ RCS.

## <a name="resolution"></a>القرار

في حالة اختلاف معرفات المستأجرين، فإنك تواجه المشكلة الموضحة في هذه المقالة. وإذا كانا متشابهين، فهذا يعني انك تواجه مشكله غير مرتبطة. في هذه الحالة، نوصي بالاتصال بدعم Microsoft.

### <a name="solution-1"></a>الحل 1

قم بتسجيل الدخول إلى بيئة RCS الخاصة بك إلى نفس المستأجر الذي تم تسجيل الدخول إليه في بيئة التمويل الخاصة بك. ثم قم بإنشاء ونشر الميزة الضريبية.

### <a name="solution-2"></a>الحل 2

شارك الميزة الضريبية مع المستأجر المالي في RCS.

1. في RCS، انتقل إلى **ميزات العولمة** \> **حساب الضريبة**.
2. حدد الميزة المراد مشاركتها، ثم في علامة التبويب **المؤسسات**، حدد **مشاركة مع**.
3. في حقل **اسم مجال المؤسسة**، أدخل اسمًا. علي سبيل المثال، قم بإدخال **contoso.onmicrosoft.com**.
4. حدد **مشاركة**.

![شارك مع مربع الحوار المنسدل للمؤسسة الخارجية.](media/ShareTaxFeature.png)
