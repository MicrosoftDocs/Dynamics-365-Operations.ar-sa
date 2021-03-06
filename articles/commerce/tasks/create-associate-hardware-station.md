---
title: " إنشاء وربط محطة أجهزة"
description: يتناول هذا الإجراء كيفية إنشاء محطة أجهزة جديدة.
author: jashanno
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: RetailHardwareStation, RetailStoreTable
audience: Application User
ms.reviewer: josaw
ms.search.region: Global
ms.search.industry: Retail
ms.author: jashanno
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: adbd5ef1cafe778cf897aafb05c77fca89be3e20
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 01/15/2021
ms.locfileid: "4964910"
---
# <a name="create-and-associate-a-hardware-station"></a> إنشاء وربط محطة أجهزة

[!include [banner](../includes/banner.md)]

يتناول هذا الإجراء كيفية إنشاء محطة أجهزة جديدة. وسيتم إنشاء ملف تعريف لجهاز جديد واستخدامه لإضافة محطات أجهزة جديدة إلى متجر محدد مسبقًا (القناة). ويستخدم هذا الإجراء شركة USRT في بيانات العرض التوضيحي.

1. انتقل إلى أساسيات التجارة > القنوات >... > .. > .. > ملفات تعريف ‏‫محطات الأجهزة‬.
2. انقر فوق "جديد".
3. في حقل "‏‫معرف محطة الأجهزة‬"، اكتب "TestHWProfile".
4. في حقل "الاسم"، اكتب قيمة.
5. في حقل "‏‫رقم المنفذ‬"، أدخل رقمًا.
6. في حقل "‏‫ملف تعريف الأجهزة‬"، انقر فوق زر القائمة المنسدلة لفتح البحث.
7. في القائمة، قم بالبحث عن السجل المطلوب وحدده.
8. في القائمة، انقر فوق الارتباط في الصف المحدد.
9. في حقل "‏‫اسم الحزمة‬"، انقر فوق زر القائمة المنسدلة لفتح البحث.
10. في القائمة، انقر فوق الارتباط في الصف المحدد.
    * هذه هي الحزمة القياسية التي تأتي مع البيئة الجديدة. قد يختلف رقم الإصدار.  
11. انقر فوق حفظ.
12. قم بإغلاق الصفحة.
13. انتقل إلى Retail and Commerce > القنوات > جميع المتاجر.
14. في القائمة، حدد الصف 17.
    * إذا كنت تستخدم شركة بيانات العرض التوضيحي USRT، فهذا هو متجر هيوستن.  
15. في القائمة، انقر فوق الارتباط في الصف المحدد.
16. قم بتبديل التوسيع لقسم ‏‫محطات الأجهزة‬.
17. وانقر فوق إضافة.
18. في القائمة، قم بوضع علامة للصف المحدد.
19. في حقل "‏‫معرف ملف التعريف‬"، انقر فوق زر القائمة المنسدلة لفتح البحث.
20. في القائمة، قم بالبحث عن السجل المطلوب وحدده.
    * يجب أن يمثل هذا ملف التعريف لمحطة الأجهزة الجديدة الذي تم إنشاؤه في الخطوات السابقة.  
21. في القائمة، انقر فوق الارتباط في الصف المحدد.
22. في حقل "اسم المضيف"، اكتب قيمة.
23. في حقل "‏‫معرف الوحدة الطرفية EFT‬"، اكتب قيمة.
24. انقر فوق "حفظ".



[!INCLUDE[footer-include](../../includes/footer-banner.md)]