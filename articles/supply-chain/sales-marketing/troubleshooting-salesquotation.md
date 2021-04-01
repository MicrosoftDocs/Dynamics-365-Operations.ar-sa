---
title: استكشاف أخطاء عروض أسعار المبيعات وإصلاحها
description: يوضح هذا الموضوع كيفية إصلاح المشكلات التي قد تواجهها أثناء العمل مع عروض أسعار المبيعات.
author: SmithaNataraj
manager: tfehr
ms.date: 09/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SalesQuotationTable, SalesQuotationTableListPage
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: smnatara
ms.search.validFrom: 2020-9-16
ms.dyn365.ops.version: Release 10.0.14
ms.openlocfilehash: 9a9cc821d2fe9accad1dae210271682cdd2ce4ba
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 02/15/2021
ms.locfileid: "5232196"
---
# <a name="troubleshoot-sales-quotations"></a><span data-ttu-id="afb92-103">استكشاف أخطاء عروض أسعار المبيعات وإصلاحها</span><span class="sxs-lookup"><span data-stu-id="afb92-103">Troubleshoot sales quotations</span></span>

<span data-ttu-id="afb92-104">يوضح هذا الموضوع كيفية إصلاح المشكلات التي قد تواجهها أثناء العمل مع عروض أسعار المبيعات.</span><span class="sxs-lookup"><span data-stu-id="afb92-104">This topic describes how to fix issues that you might encounter while you work with sales quotations.</span></span>

## <a name="i-cant-change-the-sales-quantity-of-a-sales-quotation-for-a-service-item"></a><span data-ttu-id="afb92-105">لا يمكنني تغيير كمية المبيعات لعرض أسعار المبيعات لصنف خدمة.</span><span class="sxs-lookup"><span data-stu-id="afb92-105">I can't change the sales quantity of a sales quotation for a service item.</span></span>

### <a name="issue-description"></a><span data-ttu-id="afb92-106">وصف المشكلة</span><span class="sxs-lookup"><span data-stu-id="afb92-106">Issue description</span></span>

<span data-ttu-id="afb92-107">إذا حاولت تعيين كمية مبيعات (الحقل **SalesQty**) لصنف من النوع *خدمة* على بند عرض أسعار مبيعات، ستتلقى الرسالة التالية: "التحديث غير مسموح لحقل الكمية."</span><span class="sxs-lookup"><span data-stu-id="afb92-107">If you try to set a sales quantity (**SalesQty** field) for an item of the *Service* type on a sales quotation line, you will receive the following message: "Update not allowed for field Quantity."</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="afb92-108">حل المشكلة</span><span class="sxs-lookup"><span data-stu-id="afb92-108">Issue resolution</span></span>

<span data-ttu-id="afb92-109">لا يمكنك تعيين كمية مبيعات للمنتجات التي تعد أصناف خدمة.</span><span class="sxs-lookup"><span data-stu-id="afb92-109">You can't set a sales quantity for products that are service items.</span></span> <span data-ttu-id="afb92-110">على سبيل المثال، إذا قمت بتقديم خدمة لتثبيت صنف، فلا يكون هذا الأمر منطقيًا لتسجيل كمية، بسبب عدم وجود صنف فعلي.</span><span class="sxs-lookup"><span data-stu-id="afb92-110">For example, if you offer a service to install an item, it doesn't make sense to record a quantity, because there is no physical item.</span></span> <span data-ttu-id="afb92-111">توجد خدمة فقط.</span><span class="sxs-lookup"><span data-stu-id="afb92-111">There is only a service.</span></span>



[!INCLUDE[footer-include](../../includes/footer-banner.md)]