---
title: تعيين مستخدمين إلى أدوار أمان
description: للوصول إلى Microsoft Dynamics 365 for Finance and Operations, Enterprise edition، يجب تعيين المستخدمين إلى أدوار الأمان.
author: maertenm
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysSecRolesEditUsers, SysSecAssignmentQueryLookup, SysQueryForm, SysSecRoleExcludeUsers
audience: Application User
ms.reviewer: margoc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: maertenm
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 55cb085bb5170aa4894a2240a12f6ca451b922fb
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 01/29/2019
ms.locfileid: "349942"
---
# <a name="assign-users-to-security-roles"></a>تعيين مستخدمين إلى أدوار أمان

[!include [task guide banner](../../includes/task-guide-banner.md)]

للوصول إلى Microsoft Dynamics 365 for Finance and Operations, Enterprise edition، يجب تعيين المستخدمين إلى أدوار الأمان. يوضح هذا الإجراء كيف يمكن لمسؤولي النظام تعيين مستخدمين إلى أدوار تلقائيًا، استنادًا إلى بيانات العمل. شركة بيانات العرض التوضيحي التي تم استخدامها لإنشاء هذا الإجراء هي USMF.


## <a name="automatically-assign-users-to-roles"></a>قم بتعيين مستخدمين إلى أدوار تلقائيًا
1. انتقل إلى إدارة النظام > الأمان > تعيين مستخدمين للأدوار.
2. في الشجرة، حدد "المشرف على المحاسبة".
    * حدد الدور الذي تريده لتكوين القاعدة له. في هذا المثال، حدد المشرف على المحاسبة.  
3. انقر فوق "إضافة قاعدة" لفتح مربع حوار الإسقاط‬.
4. في القائمة، قم بالبحث عن السجل المطلوب وحدده.
    * حدد الاستعلام لاستخدام هذه القاعدة.  
5. في القائمة، انقر فوق الارتباط في الصف المحدد.
6. انقر فوق "تحرير استعلام".
    * قم بتحرير الاستعلام، حسب الحاجة.  
7. انقر فوق "موافق".

## <a name="exclude-users-from-automatic-role-assignment"></a>استبعاد المستخدمين من تعيين الدور التلقائي
1. قم بإغلاق الصفحة.
2. انتقل إلى إدارة النظام > الأمان > تعيين مستخدمين للأدوار.
3. في الشجرة، حدد "المشرف على المحاسبة".
    * حدد دورًا. في هذا المثال، حدد المشرف على المحاسبة.  
4. انقر فوق تعيين/استبعاد المستخدمين يدويًا.
5. في القائمة، قم بوضع علامة للصف المحدد.
    * حدد مستخدم.  
6. انقر فوق "استبعاد من الدور".
    * انقر فوق استبعاد من الدور لاستبعاد المستخدمين المحددين من الدور. لإزالة الاستبعادات، حدد المستخدمين الذين تريد إزالة استبعادهم، ثم انقر فوق حالة إعادة التعيين. عند إزالة استبعاد بإعادة تعيين حالة المستخدم، فإنه يتم تعيين دور المستخدم تلقائيًا مرة أخرى. ومع ذلك، لا يتم تعيين المستخدم على الفور على الدور أو المستبعد من الدور عندما تقوم بإعادة تعيين الحالة. بدلاً من ذلك، إما يتم تعيين المستخدم إلى الدور أو إزالته منه في المرة التالية التي يتم فيها تشغيل تعيين الدور التلقائي.  

