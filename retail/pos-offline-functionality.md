---
title: "وظائف دون الاتصال لنقطة البيع"
description: "توفر هذه المقالة معلومات حول وضع العمل دون اتصال لنقطة البيع الحديثة للبيع بالتجزئة، حيث أجهزة نقاط البيع تتبدل تلقائيًا من قاعدة بيانات القناة إلى قاعدة بيانات دون اتصال إذا لم يتوفر خادم البيع بالتجزئة. تتضمن أيضًا هذه المقالة معلومات عامة حول الإعداد لوضع العمل دون اتصال، وتشرح مزامنة البيانات التي تحدث بين قاعدة البيانات غير المتصلة وقاعدة بيانات القناة."
author: josaw1
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: IT Pro
ms.reviewer: annbe
ms.search.scope: AX 7.0.0, Operations, Core, Retail
ms.custom: 27041
ms.assetid: 20b51874-8912-40cf-9296-864df707315a
ms.search.region: Global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 0c6a7bdc4ba82dd57ab3e395e6dfb0ae4de31fc4
ms.openlocfilehash: ef4d20b3302e4a420c7013b77a57ebdfa99fe6a3
ms.lasthandoff: 03/31/2017


---

# <a name="pos-offline-functionality"></a>وظائف دون الاتصال لنقطة البيع

[!include[banner](includes/banner.md)]


توفر هذه المقالة معلومات حول وضع العمل دون اتصال لنقطة البيع الحديثة للبيع بالتجزئة، حيث أجهزة نقاط البيع تتبدل تلقائيًا من قاعدة بيانات القناة إلى قاعدة بيانات دون اتصال إذا لم يتوفر خادم البيع بالتجزئة. تتضمن أيضًا هذه المقالة معلومات عامة حول الإعداد لوضع العمل دون اتصال، وتشرح مزامنة البيانات التي تحدث بين قاعدة البيانات غير المتصلة وقاعدة بيانات القناة.

<a name="overview"></a>نظرة عامة
--------

‏‫في "نقطة البيع بالتجزئة الحديثة"، ينتقل جهاز نقطة البيع إلى الوضع دون اتصال عند عدم توفر خادم البيع بالتجزئة. ولذلك، في حالة فقد الاتصال بخادم البيع بالتجزئة، فإنه يتم تحويل "نقطة البيع بالتجزئة الحديثة" تلقائياً إلى قاعدة بيانات دون الاتصال.‬ وأثناء عملية مبيعات، إذا لم ينجح طلب بيانات ضمن فترة المهلة التي تم تكوينها في ملف التعريف غير المتصل، تنتقل نقطة البيع بالتجزئة الحديثة تلقائياً إلى قاعدة بيانات غير المتصلة وتواصل حركة البيع. وعندما يكون جهاز نقطة البيع في وضع دون الاتصال، تحاول "نقطة البيع بالتجزئة الحديثة" إعادة الاتصال بخادم البيع بالتجزئة بعد فترة محاولة إعادة الاتصال التي تم تكوينها في ملف التعريف غير المتصل. تحدث محاولة إعادة الاتصال هذه في بداية الحركة فقط.

### <a name="determining-the-connection-mode-of-retail-modern-pos"></a>تحديد وضع الاتصال "لنقطة البيع بالتجزئة الحديثة"

يشير رأس الحالة في "نقطة البيع بالتجزئة الحديثة" إلى حالة الاتصال الحالية، وتعرض نافذة **حالة الاتصال** إطار حالة آخر محاولة للمزامنة مع قاعدة بيانات دون اتصال. [![حالة الاتصال](./media/status.png)](./media/status.png)

### <a name="creating-a-button-to-manually-switch-between-online-and-offline-modes"></a>إنشاء زر للتبديل بين وضعي الاتصال ودون الاتصال يدويًا

يمكنك إضافة زر إلى "نقطة البيع بالتجزئة الحديثة" للتبديل بين وضعي الاتصال ودون الاتصال يدويًا. أنشئ زر لعملية نقطة البيع **917 – حالة اتصال قاعدة البيانات**. ويكون اسم هذا الزر هو **قطع الاتصال** عند توصيل "نقطة البيع بالتجزئة الحديثة" بخادم البيع بالتجزئة و**الاتصال** عندما يكون غير متصل. يمكنك استخدام هذا الزر لعرض الاتصال، ولقطع الاتصال بخادم البيع بالتجزئة أو الاتصال به. [![زر قطع الاتصال في نقطة البيع بالتجزئة الحديثة](./media/details-1024x537.png)](./media/details.png)

## <a name="setup"></a>إعداد
‏‫لتمكين دعم دون الاتصال لجهاز نقطة البيع (تسجيل)، قم بتعيين خيار **‬‏‫الدعم دون اتصال‬‏‫** إلى **نعم** في صفحة **التسجيل**. ويتم إنشاء وحدة قاعدة بيانات قناة جديدة وإضافتها إلى مجموعة بيانات قناة المتجر.‬ وقم بتشغيل كافة جداول التوزيع المطلوبة لإنشاء حزم البيانات لقاعدة البيانات دون اتصال. ‏‫وبعد ذلك، قم بتثبيت النسخة غير المتصلة من "نقطة البيع بالتجزئة الحديثة". وتُنشئ عملية التثبيت قاعدة بيانات دون اتصال. بالإضافة إلى ذلك، قم بتثبيت Microsoft SQL Server 2014 Express إذا كان ذلك مطلوباً.‬ بدء تشغيل مزامنة البيانات في وضع دون الاتصال بعد أول تسجيل دخول إلى "نقطة البيع بالتجزئة الحديثة".

## <a name="data-synchronization"></a>مزامنة البيانات
يتم استخدام "جدولة" البيع بالتجزئة لإرسال البيانات الرئيسية إلى قاعدة بيانات دون الاتصال. وبشكل افتراضي، عند تشغيل جدولة توزيع، يتم إرسال تغييرات البيانات إلى كلٍّ من قاعدة بيانات القناة وقاعدة بيانات دون الاتصال. وتتضمن نقطة البيع بالتجزئة الحديثة مكتبة المزامنة المتزامنة، التي تقوم بتنزيل أي حزم بيانات متاحة وإدراجها في قاعدة البيانات غير المتصلة. إذا تم إنشاء أي حركات في وضع دون الاتصال، تقوم "نقطة البيع بالتجزئة الحديثة" بتحميلها إلى خادم البيع بالتجزئة، بحيث يمكنك إدراجها في قاعدة بيانات القناة. ويمكن أن تحدث مزامنة البيانات في وضع دون الاتصال فقط في حالة تشغيل "نقطة البيع بالتجزئة الحديثة". [![مزامنة غير متصلة بالإنترنت](./media/offline-sync-1024x521.png)](./media/offline-sync.png)



