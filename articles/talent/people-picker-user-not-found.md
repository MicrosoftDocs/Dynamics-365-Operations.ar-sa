---
title: عدم العثور على مستخدم في "منتقي الأشخاص" في Attract أو Attract
description: يشرح هذا الموضوع الخطوات التي يجب اتخاذها عند عدم ظهور مستخدمين في الشركة في "منتقي الأشخاص" في التطبيق Attract أو Onboard في Dynamics 365 for Talent.
author: ChrisChua
manager: AnnBe
ms.date: 01/22/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: chrichua
ms.search.validFrom: 2019-01-22
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 2d4a74ee2cc65153c1f9fdc1b42c2fc440d188d6
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 01/29/2019
ms.locfileid: "303164"
---
# <a name="azure-active-directory-users-not-found-in-people-picker"></a>لم يتم العثور على مستخدمي Azure Active Directory في منتقي الأشخاص

[!include [banner](includes/banner.md)]

## <a name="issue"></a>إصدار

لا يظهر بعض المستخدمين الموجودين في Microsoft Azure Active Directory (Azure AD) للمستأجر عند البحث عن الاسم في "منتقي الأشخاص" في التطبيق Attract أو Onboard في Dynamics 365 for Talent.

## <a name="cause"></a>السبب

بعض أنواع المستخدمين غير مدعومة حاليًا في التطبيقين Attract وOnboard. تأكد من أن المستخدم ليس مستخدم ضيف متاجرة بين عمل وعمل (B2B) في Azure AD. تتوفر معلومات عن "نوع المستخدم" في لوحة Azure Active Directory في مدخل Azure.

للحصول على مزيد من المعلومات حول Azure B2B، راجع [ما المقصود بوصول المستخدم الضيف في Azure Active Directory B2B](https://docs.microsoft.com/en-us/azure/active-directory/b2b/what-is-b2b).

بالنسبة إلى المستخدمين من غير B2B، قد تكون لدى بعض المستخدمين خاصية "نوع المستخدم" غير كاملة على كائن **المستخدم**. يمكن التحقق من هذا الأمر وإصلاحها باستخدام وحدة Azure AD Powershell. لمزيد من المعلومات، راجع [Azure AD](https://docs.microsoft.com/en-us/powershell/module/azuread/?view=azureadps-2.0).

## <a name="resolution"></a>الدقة

لإكمال الخطوات التالية لحل هذه المشكلة، ستحتاج إلى أذونات "المسؤول العمومي" على مستأجر Azure Active Directory أو أذونات **User.ReadWrite.All**.

للتحقق من "نوع المستخدم" للمستخدم المتأثر.

```
PS C:\>Get-AzureADUser -ObjectId "testUpn@tenant.com"
```
يرجع الأمر المعلومات التالية.
```
ObjectId                             DisplayName UserPrincipalName      UserType
--------                             ----------- -----------------      --------
5e8b0f4d-2cd4-4e17-9467-b0f6a5c0c4d0 New user    testUpn@tenant.com     
```
لاحظ خاصية **UserType** على المستخدم. إذا كانت خاصية **UserType** فارغة، على سبيل المثال، ليست "عضو" أو "ضيف"، فحدّث **UserType** باستخدام الأمر التالي.

```
PS C:\>Set-AzureADUser -ObjectId "testUpn@tenant.com" -UserType Member
```