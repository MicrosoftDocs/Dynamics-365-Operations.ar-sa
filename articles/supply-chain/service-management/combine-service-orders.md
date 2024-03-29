---
title: تجميع أوامر الخدمة
description: يمكنك تجميع أوامر الخدمة.
author: sorenva
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SMAServiceOrderTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: sorenand
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: f89c60561746ac9f1c2e9d611089bfac69089081
ms.sourcegitcommit: 9166e531ae5773f5bc3bd02501b67331cf216da4
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 05/03/2022
ms.locfileid: "8676764"
---
# <a name="combine-service-orders"></a>تجميع أوامر الخدمة   

[!include [banner](../includes/banner.md)]


عندما تقوم بإنشاء بنود أوامر الخدمة تلقائياً في نموذج **اتفاقيات الخدمات**، يمكنك اختيار أحد الخيارات التالية لتحديد الطريقة التي ترغب في تجميعهم حسبها:

  - **بواسطة اتفاقية الخدمات**

  - **بواسطة مهمة الخدمة**

  - **بواسطة الموظف**

  - **بواسطة كائن الخدمة**

## <a name="example"></a>مثال

تقوم بإنشاء اتفاقية خدمة بتاريخ بدء في 03-31-2007. في الحقل **تجميع أوامر الخدمة**، حدد **بواسطة كائن الخدمة**. ثم تقوم بعد ذلك بإنشاء بنود اتفاقية الخدمة التالية:

<table>
<colgroup>
<col />
<col />
<col />
<col />
<col />
<col />
</colgroup>
<thead>
<tr class="header">
<th><p>رقم سطر الاتفاقية</p></th>
<th><p>نوع الحركة</p></th>
<th><p>الوصف</p></th>
<th><p>الفترة</p></th>
<th><p>كائن الخدمة</p></th>
<th><p>تاريخ البدء</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>1</p></td>
<td><p><strong>ساعة</strong></p></td>
<td><p>SAL1</p></td>
<td><p>أسبوعيًا</p></td>
<td><p>X1-</p></td>
<td><p>01/04/2007</p></td>
</tr>
<tr class="even">
<td><p>2</p></td>
<td><p><strong>ساعة</strong></p></td>
<td><p>SAL2</p></td>
<td><p>نصف أسبوعي</p></td>
<td><p>X-2</p></td>
<td><p>01/04/2007</p></td>
</tr>
<tr class="odd">
<td><p>3</p></td>
<td><p><strong>ساعة</strong></p></td>
<td><p>SAL3</p></td>
<td><p>أسبوعيًا</p></td>
<td><p>X-2</p></td>
<td><p>01/04/2007</p></td>
</tr>
</tbody>
</table>


ولم تقم بتحديد إطارات زمنية لأي بند من بنود اتفاقية الخدمة. لذلك، لن يتم نقل بنود اتفاقية الخدمة من اليوم المحسوب الذي وقعت فيه.

بعد ذلك، قمت بإنشاء بنود أوامر الخدمة من النموذج **إنشاء أوامر الخدمة** من 04-01-2007 حتى 04-30-2007.

وفي الإجمالي تم إنشاء 10 أوامر خدمة. ونظرًا لأن الإعداد المجمع الذي قمت بتحديده كان **بواسطة كائن الخدمة**، فإن كافة أوامر الخدمة التي تم إنشاؤها تتضمن بنود أمر خدمة مع كائن خدمة معين واحد فقط. ويتم تجميع بنود أوامر الخدمة التي تم إنشاؤها من اتفاقية الخدمة والتي لها نفس تاريخ الخدمة ونفس الكائن في نفس أمر الخدمة.


> [!NOTE]
> <P>في هذا المثال، لا يتضمن التقويم المحدد في نموذج <STRONG>محددات إدارة الخدمة</STRONG> أي أيام مغلقة.</P>



يحدث تجميع بنود أوامر الخدمة الإضافية في أوامر الخدمة وفقًا لأي إطار زمني تقوم بتحديده ضمن بنود اتفاقية الخدمة.

## <a name="see-also"></a>راجع أيضًا

[إنشاء أوامر الخدمة تلقائيًا](create-service-orders-automatically.md)

  




[!INCLUDE[footer-include](../../includes/footer-banner.md)]