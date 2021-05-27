---
title: لا يمكنك إزالة بُعد التنبؤ بطلب المستودع من بنود التنبؤ
description: لا يمكنك إزالة بُعد التنبؤ بطلب المستودع من بنود التنبؤ.
author: ChristianRytt
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: ForecastSales
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 6b643c4fe51ae6ce73b34ab81d4e458dcd5032df
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026238"
---
# <a name="you-cant-remove-the-warehouse-demand-forecast-dimension-from-forecast-lines"></a><span data-ttu-id="b8848-103">لا يمكنك إزالة بُعد التنبؤ بطلب المستودع من بنود التنبؤ</span><span class="sxs-lookup"><span data-stu-id="b8848-103">You can't remove the Warehouse demand forecast dimension from forecast lines</span></span>

<span data-ttu-id="b8848-104">رقم KB: 4614408</span><span class="sxs-lookup"><span data-stu-id="b8848-104">KB number: 4614408</span></span>

## <a name="symptoms"></a><span data-ttu-id="b8848-105">العلامات</span><span class="sxs-lookup"><span data-stu-id="b8848-105">Symptoms</span></span>

<span data-ttu-id="b8848-106">تحدث هذه المشكلة في حالة عدم تعيين **المستودع** على علامة التبويب **أبعاد التنبؤ** للصفحة **معلمة التنبؤ بالطلب**.</span><span class="sxs-lookup"><span data-stu-id="b8848-106">This issue occurs when the **Warehouse** dimension isn't assigned on the **Forecast dimensions** tab of the **Demand forecasting parameter** page.</span></span> <span data-ttu-id="b8848-107">ومع ذلك، يتم عرض العمود **المستودع** في الصفحة **التنبؤ بالطلب** (**التخطيط الرئيسي \> التنبؤ \> كيان التنبؤ اليدوي \> ‏‫بنود التنبؤ بالطلب**).</span><span class="sxs-lookup"><span data-stu-id="b8848-107">Nevertheless, the **Warehouse** column is shown on the **Demand forecast** page (**Master planning \> Forecasting \> Manual forecast entity \> Demand forecast lines**).</span></span>

## <a name="resolution"></a><span data-ttu-id="b8848-108">الدقة</span><span class="sxs-lookup"><span data-stu-id="b8848-108">Resolution</span></span>

<span data-ttu-id="b8848-109">لا تؤثر الإعدادات الموجودة على علامة التبويب **أبعاد التنبؤ** في الصفحة **معلمة التنبؤ بالطلب** على الصفحة **التنبؤ بالطلب**.</span><span class="sxs-lookup"><span data-stu-id="b8848-109">The settings on the **Forecast dimensions** tab of the **Demand forecasting parameter** page don't affect the **Demand forecast** page.</span></span> <span data-ttu-id="b8848-110">وتتحكم في التنبؤ الأساسي الذي تم إنشاؤه وعرضه في التنبؤ بالطلب الذي تم تعديله.</span><span class="sxs-lookup"><span data-stu-id="b8848-110">They control the baseline forecast that is generated and shown in the adjusted demand forecast.</span></span> <span data-ttu-id="b8848-111">ومع ذلك، لا تتحكم هذه العناصر في الأبعاد المطلوبة للتنبؤ بالطلب "الحقيقي".</span><span class="sxs-lookup"><span data-stu-id="b8848-111">However, they don't control the dimensions that are required for the "real" demand forecast.</span></span> <span data-ttu-id="b8848-112">ومن خلال تخويل السجلات التي ستم عرضها في الصفحة **التنبؤ بالطلبات التي تم تعديلها**، يمكنك تحويلها إلى إدخالات تنبؤ "حقيقية" لنموذج تنبؤ.</span><span class="sxs-lookup"><span data-stu-id="b8848-112">By authorizing the records that are shown on the **Adjusted demand forecast** page, you can convert them to "real" forecast entries for a forecast model.</span></span> <span data-ttu-id="b8848-113">ويمكن بعد ذلك استخدام هذا النموذج للتخطيط الرئيسي.</span><span class="sxs-lookup"><span data-stu-id="b8848-113">That model can then be used for master planning.</span></span>

<span data-ttu-id="b8848-114">في الصفحة **التنبؤ بالطلب**، تكون أبعاد التنبؤ "الفعلي" التي يتم عرضها في بنود التنبؤ بالطلب جزءًا من أبعاد المخزون.</span><span class="sxs-lookup"><span data-stu-id="b8848-114">On the **Demand forecast** page, the dimensions for the "real" forecast that are shown on the demand forecast lines are part of the inventory dimensions.</span></span> <span data-ttu-id="b8848-115">(يشبه هذا السلوك سلوك بنود أمر التوريد.) في حالة عدم إعداد النظام الخاص بك لاستخدام **المستودع** كبُعد مخزون إلزامي، يمكن تخصيص الصفحة لإخفاء العمود.</span><span class="sxs-lookup"><span data-stu-id="b8848-115">(This behavior resembles the behavior for sales order lines.) If your system isn't set up to use **Warehouse** as a mandatory inventory dimension, you can customize the page to hide the column.</span></span>
