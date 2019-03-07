---
title: " إنشاء وربط سجلات"
description: يوضح هذا الإجراء كيفية إنشاء سجل نقطة البيع.
author: rubencdelgado
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: RetailTerminalTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: rubendel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 07e4b9f32a3a74b273272bd0b759d35c2a963e2e
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 01/29/2019
ms.locfileid: "360637"
---
# <a name="create-and-associate-registers"></a> إنشاء وربط سجلات

[!include[task guide banner](../includes/task-guide-banner.md)]

يوضح هذا الإجراء كيفية إنشاء سجل نقطة البيع. يستخدم هذا الإجراء شركة بيانات العرض التوضيحي USRT.

1. في AX7، انتقل إلى البيع بالتجزئة والتجارة > إعداد القناة > إعداد نقطة البيع > السجلات.
2. انقر فوق "جديد".
3. في الحقل "رقم السجل" اكتب معرف السجل الجديد.
    * يتضمن "معرف السجل" عادةً أكوادًا قد تساعد على تعيين السجل إلى المتجر الذي ينتمي إليه والموقع داخل المخزن.  
4. في حقل "الاسم"، اكتب اسمًا وصفيًا للسجل.
5. في الحقل "رقم المتجر"، أدخل قيمة أو حددها.
6. في الحقل "ملف تعريف الأجهزة"، أدخل قيمة أو حددها.
    * يتم استخدام ملفات تعريف الأجهزة لتحديد الأجهزة الطرفية للبيع بالتجزئة التي سيتم توصيلها بالسجل، مثل درج الأوراق النقدية وطابعة الإيصالات.  
7. في حقل "ملف التعريف المرئي‬"، أدخل قيمة أو حددها.
    * يتم استخدام ملفات التعريف المرئية لتحديد الصور المستخدمة في خلفية نقطة البيع وصفحة تسجيل الدخول بالإضافة إلى نُسق نقطة البيع.  
8. في الحقل "رقم تسجيل نقطة بيع EFT"، اكتب قيمة.
    * يتم استخدام "رقم تسجيل نقطة بيع EFT" لإعلام معالج الدفع بمحطة الدفع الطرفية التي تُرسل طلبات التفويض. غالبًا ما تسمى هذه القيمة "معرف المحطة الطرفية" أو "TID". يمكن العثور على TID عادةً على ملصق على جهاز الدفع.  
9. انقر فوق "حفظ".

