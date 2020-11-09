---
title: استكشاف المشاكل ذات الصلة بإدراك الحلول وإصلاحها
description: يوفر هذا الموضوع استكشاف الأخطاء وإصلاحها الذي يمكن أن يساعدك في إصلاح المشكلات ذات الصلة بإدراك الحلول.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 03/16/2020
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
ms.search.validFrom: 2020-03-16
ms.openlocfilehash: 7f1a6e424996201ecae1b624c13cfc573745dc0a
ms.sourcegitcommit: 0a741b131ed71f6345d4219a47cf5f71fec6744b
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 10/13/2020
ms.locfileid: "3997268"
---
# <a name="troubleshoot-issues-related-to-solution-awareness"></a>استكشاف المشاكل ذات الصلة بإدراك الحلول وإصلاحها

[!include [banner](../../includes/banner.md)]



يوفر هذا الموضوع معلومات حول استكشاف أخطاء تكامل الكتابة الثنائية وإصلاحها بين تطبيقات Finance and Operations وCommon Data Service. على وجه التحديد، يوفر هذا الموضوع المعلومات التي يمكن أن تساعدك في إصلاح المشكلات ذات الصلة بإدراك الحلول.

> [!IMPORTANT]
> قد تتطلب بعض المشكلات التي يتناولها هذا الموضوع إما دور إدارة النظام أو بيانات اعتماد مسؤول مستأجر  Microsoft Azure Active Directory (Azure AD). يوضح القسم الخاص بكل مشكلة ما إذا كانت هناك حاجة إلى دور محدد أو بيانات اعتماد.

## <a name="error-on-the-dual-write-page"></a>خطأ في صفحة الكتابة الثنائية

في صفحة **الكتابة الثنائية** ، قد تتلقي رسالة خطأ مشابهة للمثال التالي:

*لم يتم العثور على الكيان باسم 'msdyn\_dualwriteentitymap' with namemapping='Logical' في MetadataCache.*

لإصلاح المشكلة، تأكد من تثبيت الحل الأساسي للكتابة الثنائية في Common Data Service. يُعد الحل الأساسي للكتابة الثنائية متطلبًا أساسيًا لمعرفة الحلول.
