---
title: نظره عامة على MyLeaveRequests
description: يوفر كيان MyLeaveRequests في Microsoft Dynamics 365 Human Resources قائمة بطلبات الإجازات في النظام، مقيدة (محدودة) على الطلبات التي يمكن الوصول إليها للمستخدم الحالي الذي يقوم بالاستعلام عن الكيان.
author: andreabichsel
ms.date: 02/03/2020
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.search.scope: Human Resources
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 41ef8c6fc0e896e7f2cefd94801abab610083b81
ms.sourcegitcommit: 3a7f1fe72ac08e62dda1045e0fb97f7174b69a25
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 01/31/2022
ms.locfileid: "8070844"
---
# <a name="myleaverequests-overview"></a>نظره عامة على MyLeaveRequests


[!INCLUDE [PEAP](../includes/peap-1.md)]

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
