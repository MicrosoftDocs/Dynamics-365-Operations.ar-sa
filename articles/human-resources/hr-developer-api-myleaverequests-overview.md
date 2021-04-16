---
title: نظره عامة على MyLeaveRequests
description: يوفر كيان MyLeaveRequests في Microsoft Dynamics 365 Human Resources قائمة بطلبات الإجازات في النظام، مقيدة (محدودة) على الطلبات التي يمكن الوصول إليها للمستخدم الحالي الذي يقوم بالاستعلام عن الكيان.
author: andreabichsel
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 44e23a076733bac782a0366aeba3456911522abe
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 03/31/2021
ms.locfileid: "5803623"
---
# <a name="myleaverequests-overview"></a>نظره عامة على MyLeaveRequests

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

يوفر كيان MyLeaveRequests في Microsoft Dynamics 365 Human Resources قائمة بطلبات الإجازات في النظام، مقيدة (محدودة) على الطلبات التي يمكن الوصول إليها للمستخدم الحالي الذي يقوم بالاستعلام عن الكيان.

## <a name="key"></a>مفتاح

  | اسم الخاصية | نوع البيانات |
  |---------------|-----------|
  | dataAreaId    | سلسلة    |
  | RequestId     | سلسلة    |
  | LeaveType     | سلسلة    |
  | LeaveDate     | التاريخ      |
  
## <a name="properties"></a>خصائص

  | اسم الخاصية     | نوع البيانات | مطلوب |
  |-------------------|-----------|----------|
  | dataAreaId        | سلسلة    | س        |
  | RequestId         | سلسلة    | س        |
  | LeaveType         | سلسلة    | س        |
  | LeaveDate         | التاريخ      | س        |
  | ReasonCodeId      | سلسلة    |          |
  | PersonnelNumber   | سلسلة    | س        |
  | RequestDate       | التاريخ      | س        |
  | تعليق           | سلسلة    |          |
  | الحالة            | تعداد      | س        |
  | ‏‏المقدار            | حقيقي      |          |
  | HalfDayDefinition | تعداد      |          |

## <a name="actions"></a>إجراءات

 | اسم الإجراء                               | ‏‏الوصف                                     |
 |-------------------------------------------|-------------------------------------------------|
 | [إرسال](hr-developer-api-myleaverequests-submit.md)   | أرسل الطلب لمعالجته من خلال سير العمل. |

## <a name="see-also"></a>راجع أيضًا

- [إرسال طلب إجازة إلى سير العمل](hr-developer-api-myleaverequests-submit.md)
- [المصادقة](hr-developer-api-authentication.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]