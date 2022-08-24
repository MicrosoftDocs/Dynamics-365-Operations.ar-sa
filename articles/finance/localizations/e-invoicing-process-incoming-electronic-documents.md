---
title: معالجة المستندات الإلكترونية الواردة
description: توفر هذه المقالة نظرة عامة على معالجة المستندات الإلكترونية الواردة.
author: gionoder
ms.date: 02/28/2022
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
ms.openlocfilehash: 554bc8fde3b2135eb878d885541c76ecd6d66493
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 08/12/2022
ms.locfileid: "9277290"
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
