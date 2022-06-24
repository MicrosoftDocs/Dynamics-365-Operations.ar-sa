---
title: استكشاف المشكلات ذات الصلة بإدراك الحلول وإصلاحها
description: توفر هذه المقالة معلومات استكشاف الأخطاء وإصلاحها الذي يمكن أن تساعدك على إصلاح المشكلات ذات الصلة بإدراك الحلول.
author: RamaKrishnamoorthy
ms.date: 03/16/2020
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: tfehr
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2020-01-06
ms.openlocfilehash: c280eef995664c640e382817dda9d6e1cde154c6
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 06/03/2022
ms.locfileid: "8871484"
---
# <a name="troubleshoot-issues-related-to-solution-awareness"></a>استكشاف المشكلات ذات الصلة بإدراك الحلول وإصلاحها

[!include [banner](../../includes/banner.md)]





توفر هذه المقالة معلومات عن استكشاف الأخطاء وإصلاحها في تكامل الكتابة المزدوجة بين تطبيقات التمويل والعمليات و Dataverse. على وجه التحديد، يوفر هذا الموضوع المعلومات التي يمكن أن تساعدك في إصلاح المشكلات ذات الصلة بإدراك الحلول.

> [!IMPORTANT]
> قد تتطلب بعض المشكلات التي تتناولها هذه المقالة إما منصب مسؤول النظام أو بيانات اعتماد مسؤول مستأجر Microsoft Azure Active Directory (Azure AD). يوضح القسم الخاص بكل مشكلة ما إذا كانت هناك حاجة إلى دور محدد أو بيانات اعتماد.

## <a name="error-on-the-dual-write-page"></a>خطأ في صفحة الكتابة الثنائية

في صفحة **الكتابة الثنائية**، قد تتلقي رسالة خطأ مشابهة للمثال التالي:

*لم يتم العثور على الكيان باسم 'msdyn\_dualwriteentitymap' with namemapping='Logical' في MetadataCache.*

لإصلاح المشكلة، تأكد من تثبيت الحل الأساسي للكتابة الثنائية في Dataverse. يُعد الحل الأساسي للكتابة الثنائية متطلبًا أساسيًا لمعرفة الحلول.


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]