---
title: معالجة المستندات الإلكترونية الواردة
description: يوفر هذا الموضوع نظرة عامة حول معالجة المستندات الإلكترونية الواردة.
author: dkalyuzh
ms.date: 02/28/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkalyuzh
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 9701367e1ba1f9dbd1e53deb863c10af4213a359
ms.sourcegitcommit: ffdb6794746ffe5461f9dcf34ed8e64976d22d2d
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 03/02/2022
ms.locfileid: "8371471"
---
# <a name="processing-of-incoming-electronic-documents"></a>معالجة المستندات الإلكترونية الواردة

[!include [banner](../includes/banner.md)]

يمكن استيراد المستندات الإلكترونية الواردة، مثل الفواتير الإلكترونية للبائع، ومعالجتها بطريقتين:

- يتم استرداد الملفات من القنوات الخارجية وتمريرها مباشرة إلى التطبيق المتصل. هناك، يخضعون لعملية تحويل إضافية ثم يتم استيرادهم إلى قاعدة البيانات.
- المعالجة المسبقة للملفات في خدمه الفوترة الكترونيه ويتم تمريرها بعد ذلك إلى التطبيق المتصل.

تدعم الفواتير الإلكترونية قناتين للمستندات الواردة: البريد الإلكتروني ومجلدات Microsoft SharePoint.

هناك أنواع إعداد twp لتحديد ما إذا كانت المستندات تخضع للمعالجة المسبقة أو يتم تمريرها مباشرةً إلى التطبيق المتصل الخاص بك:

- **قناة البيانات** – سيقوم النظام بتمرير المستند مباشرة إلى التطبيق المتصل.
- **قناة البيانات مع مسار المعالجة** – يمكنك إعداد إجراءات إضافية سيتم تشغيلها قبل تمرير المستند إلى التطبيق المتصل.

للحصول على معلومات حول كيفية إعداد السيناريوهات لمعالجة المستندات الإلكترونية الواردة للقنوات المختلفة، راجع [تكوين قناة بريد إلكتروني](e-invoicing-configure-email.md) و[تكوين قناة SharePoint](e-invoicing-configure-sharepoint-channel.md).
